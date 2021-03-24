# vote_counter
candidate1 = input("Enter the 1st Candidate : ")
candidate2 = input("Enter the 2nd Candidate : ")

Candi1_vote = 0
Candi2_vote = 0

voter_id = [1,2,3,4,5]

number_of_voter =len(voter_id)

while True:
	if voter_id==[]:
		print("Voting Season is over")
		if Candi1_vote> Candi2_vote :
			percent=(Candi1_vote/number_of_voter)*100
			print(candidate1, "Has Won",percent,"% Votes")
			break

		elif Candi2_vote> Candi1_vote :
			percent=(Candi2_vote/number_of_voter)*100
			print(candidate2, "Has Won",percent,"% Votes")
			break
	else:
		voter = int(input("Enter your voter id number : "))

		if voter in voter_id:
			print("Your are a voter ")
			voter_id.remove(voter)
			vote = int(input("Enter your Vote 1 or 2 : "))

			if vote==1:
				Candi1_vote+=1
				print("Thank You")


			elif vote ==2:
				Candi2_vote+=1
				print("Thank You")
		else:
			print("Your are not a voter")
