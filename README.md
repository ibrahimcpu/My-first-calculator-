import time
print("Welcome to my Calculator!")
#using loop to ask user to enter or not
while True:
    ready = input("Are you ready to Start Calculating? (yes/no): ").lower().strip()
    if ready == "yes":
        print("Start...")
        break
    elif ready == "no":
        print("Quiting........!")
        time.sleep(3)
        print("Calculator Closed")
#start the calculation       
while True:
    try:      
        choose1 = float(input("Enter first number: "))
        choose2 = input("Select option, (+, - , ×, ÷): ")
        choose3 = float(input("Enter second number: "))
    except ValueError:
         print("invalid, please insert number")
         continue
    answer = choose1 + choose3
    answer2 = choose1 - choose3
    answer3 = choose1 * choose3
    if choose3 != 0:
            answer4 = choose1 / choose3
    else:
           answer4 = None
#instructions         
    if choose2 == "+":
        print("answer: ", answer)
    elif choose2 == "-":
        print("answer: ", answer2)
    elif choose2 == "×":
        print("answer: ", answer3)
    elif choose2 == "÷":
        if choose3 != 0:         
           print("answer:", answer4)
        else:
            print("Can not divide by 0")
    else:
        print("Syntax Error!")
    stop = input("Would you like to calculate again? (yes/no)\ntype Exit to Quit: ").lower().strip()
    if stop == "yes":
        continue
    elif stop == "no":
        pause = input("Are you sure you want to Exit? (yes/no): ").lower().strip()
        if pause == "yes":
            print("Exiting.......")
            time.sleep(3)
            print("You close the Calculator.")
            exit()
        elif pause == "no":
            print("Start again!")
            continue
    elif stop == "exit":
        print("Exiting.....")
        time.sleep(5)
        print("Calculator Has Closed!")
        exit()
    else:
         continue
#the end
   
    
