# Vault Door 3

**FLAG**: `picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21}`


## Thought Process
This challenge was actually surprisingly simple. I noticed that the code itself gave away what the challenge was about. On running the code for the first time, I got 
```
apple@Luckys-MacBook-Air cryptonite_taskphase_shreyas %  /usr/bin/env /Library/Java/JavaVirtualMac
hines/jdk-22.jdk/Contents/Home/bin/java -XX:+ShowCodeDetailsInExceptionMessages -cp /Users/apple/L
ibrary/Application\ Support/Code/User/workspaceStorage/46cb8badbe09bb4ec8949ab965e63ad8/redhat.jav
a/jdt_ws/jdt.ls-java-project/bin VaultDoor3 
Enter vault password: akjldkjllsdlk
Access denied!
```
Then on further going through the code, and interpretting it piece by piece i understood more information. it was fairly easy to read and understand what was happening.

```
class VaultDoor3 {
    public static void main(String args[]) {
        VaultDoor3 vaultDoor = new VaultDoor3();
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter vault password: ");
        String userInput = scanner.next();
	String input = userInput.substring("picoCTF{".length(),userInput.length()-1);
	if (vaultDoor.checkPassword(input)) {
	    System.out.println("Access granted.");
	} else {
	    System.out.println("Access denied!");
        }
    }
```
This part of the code was checking for the password inputted. on viewing further parts of the code, it was understood that the password was the flag itself, just jumbled up, and the whole point of the challenge was to unjumble the flag. 

```
public boolean checkPassword(String password) {
        if (password.length() != 32) {
            return false;
        }
        char[] buffer = new char[32];
        int i;
        for (i=0; i<8; i++) {
            buffer[i] = password.charAt(i);
        }
        for (; i<16; i++) {
            buffer[i] = password.charAt(23-i);
        }
        for (; i<32; i+=2) {
            buffer[i] = password.charAt(46-i);
        }
        for (i=31; i>=17; i-=2) {
            buffer[i] = password.charAt(i);
        }
        String s = new String(buffer);
        return s.equals("jU5t_a_sna_3lpm12g94c_u_4_m7ra41");
    }
}
```
This was the part which was jumbling the flag. The jumbled up flag was also present which was `jU5t_a_sna_3lpm12g94c_u_4_m7ra41`
So i ran picoCTF{jU5t_a_sna_3lpm12g94c_u_4_m7ra41}, which still showed access denied so i was confused for a little while, then i remembered that `jU5t_a_sna_3lpm12g94c_u_4_m7ra41` is already jumbled up and the whole point is to unjumble it and to see what the second part of the code is actually doing. so i added a `system.out.println(buffer)` right before the function is being returned so that before the password is checked, atleast I can tell how the scrambler works and what it does. 
On running this now, i got 

```
Enter vault password: picoCTF{jU5t_a_sna_31pm12g94c_u_4_m7ra41}
jU5t_a_s1mpl3_an4gr4m_4_u_c79a21
Access denied!
```
So i got my unscrambled password `jU5t_a_s1mpl3_an4gr4m_4_u_c79a21`, which on running again in the code wrapped in picoCTF ofcourse, i got 
```
Enter vault password: picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21}
jU5t_a_sna_31pm12g94c_u_4_m7ra41
Access granted.
```
which gave us our original scrambled password (jU5t_a_sna_31pm12g94c_u_4_m7ra41) again. 

Hence our flag was `picoCTF{jU5t_a_s1mpl3_an4gr4m_4_u_c79a21}`

##

## What i learnt through this challenge
Reading through code and understanding what it's meant to do. This challenge was a perfect example of that and gave me a ton of confidence boost because i was able to read the code perfectly. 
##

## Mistakes
while recreating the flag, i forgot to put picoCTF{} around the jumbled flag initially.
##


#