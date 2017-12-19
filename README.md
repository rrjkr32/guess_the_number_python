# guess_the_number_python
A mini game in python

      from random import *

      def main():
              ip=input("Guess a number between 1 and 100:\n")

              op=randint(1,100)
              cnt=1
              while int(ip)!=op:
                  if int(ip)>op:
                      ip=input("Too high ,Guess again:\n")
                  else:
                      ip=input("Too low ,Guess again:\n")
                  cnt+=1
              print("You won in {} times\nThe number was {}\nThanks for playing!".format(cnt,op))

      main()
