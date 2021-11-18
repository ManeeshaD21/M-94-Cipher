# encryption code
```
{
def translate(startLetters, endLetters, spot):
    #find the letter at (spot) in the startLetters string. 
  
    #find the location of the letter in the endLetters string.

  return endLetters.find(startLetters[spot])


def rotate(alphabet):
    #move the first letter of the alphabet to the end
    #shift all the letters
 

  return alphabet[1:]+alphabet[0] #this has been rotated


def main():
    
    alpha =  "ABCDEFGHIJKLMNOPQRSTUVWXYZ"
    disk1 = "EKMFLGDQVZNTOWYHXUSPAIBRCJ"
    disk2 = "AJDKSIRUXBLHWTMCQGZNPYFVOE"
    disk3 = "BDFHJLCPRTXVZNYEIWGAKMUSQO"
    disk4 = "QNISOFJVULDXHZBCYPAKEMRGWT"
    disk5 = "XVTPZGYHRAEFIUWBJNMOKSCLQD"
    
   

    

    # get a message from the user


    message = input("give a 5 letter message: ").upper()
    letter = message[0]
    encoded = ""
    for letter in message:
      if alpha.find(letter) >= 0:
      # Find location of letter in alphabet
        pos = alpha.find(letter)

        #pass this letter through rotor1
        pos = translate(alpha, disk1, pos) #starting, ending, current position
        pos = translate(alpha, disk2, pos)
        pos = translate(alpha, disk3, pos)
        pos = translate(alpha, disk4, pos) #starting, ending, current position
        pos = translate(alpha, disk5, pos)
        

        #Translate back from position to a letter
        encoded += alpha[pos]

        # Now that we have been through one pass, adjust any of the rotors that need to be rotated.
        disk1 = rotate(disk1)
        if pos != 0 and pos % 26 == 0: disk2 = rotate(disk1)
        if pos != 0 and pos % 26 == 0: disk3 = rotate(disk3)
        if pos != 0 and pos % 26 == 0: disk4 = rotate(disk4)
        if pos != 0 and pos % 26 == 0: disk5 = rotate(disk5)

      
    print(encoded) #This one letter has been encoded


main()
}
```
#decryption code
