# guess_the_number_python
A mini game in python

                  from random import *
            def valip(ip):
                while   not ip.isdigit() or not (1<=int(ip)<=100):
                         ip=input("That is not Valid,Guess a number between 1 and 100:\n")
                return ip
            def main():
                    ip=input("Guess a number between 1 and 100:\n")

                    op=randint(1,100)
                    cnt=1

                    ip=valip(ip)

                    while int(ip)!=op:
                        ip=valip(ip)
                        if  int(ip)==op:
                            break
                        if int(ip)>op:
                            ip=input("Too high ,Guess again:\n")
                        else:
                            ip=input("Too low ,Guess again:\n")
                        cnt+=1
                    print("You won in {} times\nThe number was {}\nThanks for playing!".format(cnt,op))

            main()
