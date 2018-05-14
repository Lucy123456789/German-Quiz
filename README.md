# German-Quiz
# German language quiz

# Quiz to practise German, multiple modules which can be selected as required.


## Text menu in Python
      
def print_menu(): 
    print (30 * "-" , "MENU" , 30 * "-")
    print ("1. Menu Option 1")
    print ("2. Verbs in the present tense")
    print ("3. Menu Option 3")
    print ("4. Menu Option 4")
    print ("5. Exit")
    print (67 * "-")
  
loop=True      
  
while loop:          ## While loop which will keep going until loop = False
    print_menu()    ## Displays menu
    choice = input("Enter your choice [1-5]: ")
     
    if choice == 1:     
        print ("Menu 1 has been selected")
        ## You can add your code or functions here
    elif choice == 2:
        print ("Menu 2 has been selected")
        # Verbs in the present tense

		questions = ["1. I live in Berlin", 
					"2. He drinks coffee", 
					"3. She plays tennis", 
					"4. We are learning German", 
					"5. Carla and Sophia are playing football",
					"6. Where do you come from? (informal)",
					"7. Where do you come from? (formal",
					"8. Where do you live? (informal)",
					"9. Where do you live? (formal)",
					"10. Do you Skype? (informal)",
					"11. Do you Skype? (formal)"]

		correct_choices = [{"ich wohne in berlin"},
					{"er trinkt kaffee"},
					{"sie spielt tennis"},
					{"wir lernen deutsch"},
					{"carla and sophia spielen fußball"},
					{"woher kommst du?"},
					{"woher kommen sie?"},
					{"wo wohnst du?"},
					{"wo wohnen sie?"},
					{"skypst du?"},
					{"skypen sie?"}] 

		answers = ["Ich wohne in Berlin.",
					"Er trinkt Kaffee",
					"Sie spielt Tennis",
					"Wir lernen Deutsch",
					"Carla and Sophia spielen Fußball",
					"Woher kommst du?",
					"Woher kommen Sie?",
					"Wo wohnst du?",
					"Wo wohnen Sie?"
					"Skypst du?",
					"Skypen Sie?"]

		def quiz():
    		score = 0
    		for question, correct_choice, answer in zip(questions, correct_choices, answers):
        		print(question)
        		user_answer = input("Translate into German: ").lower()
        		if user_answer in correct_choice:
           			print("Correct:", answer)
           			score += 1
        		else:
           			print("Incorrect:", answer)
    		print(score, "out of", len(questions), ", which is", round(float(score / len(questions)) * 100, 1), "%")

		if __name__ == "__main__":
    		quiz()

    elif choice == 3:
        print ("Menu 3 has been selected")
        ## You can add your code or functions here
    elif choice == 4:
        print ("Menu 4 has been selected")
        ## You can add your code or functions here
    elif choice == 5:
        print ("Menu 5 has been selected")
        ## You can add your code or functions here
        loop=False # This will make the while loop to end as not value of loop is set to False
    else:
        # Any integer inputs other than values 1-5 we print an error message
        raw_input("Wrong option selection. Enter any key to try again..")
         
