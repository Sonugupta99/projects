# projects
nominee1 = input("Enter the name of 1st nominees")
nominee2 = input("Enter the name of 2nd nominees")
nm1_votes=0
nm2_votes=0
voter_id=[1,2,3,4,5,6,7,8,9]
no_of_voters=len(voter_id)
while True:
    if voter_id==[]:  # to check when voter list is completed
        print("voting session is over !!!")
        if nm1_votes>nm2_votes:
            percent=(nm1_votes/no_of_voters)*100    #to calculate the percentage
            print(nominee1,"has won the election with ",percent,"% of votes")
            break    # to get rid of infinite loop
        elif nm2_votes>nm1_votes:
            percent=(nm2_votes/no_of_voters)*100
            print(nominee2,"has won the election with",percent,"% of votes")
            break
        else:
            print("both have equal number of voters !!!! Goverment will decide who will rule")
            break
    voter=int(input("Enter your voter id: " ))+
    if voter in voter_id:
        print("your are a voter")
        voter_id.remove(voter)  # we will remove that again some voter can't vote
        print("-------------------")
        print("To give vote to",nominee1,"Press 1")
        print("To give vote to",nominee2,"Press 2")
        print("-------------------")
        vote=int(input("Enter your precious vote :"))
        if vote==1:
            nm1_votes +=1
            print(nominee1,"Thanks yoi to give your important to them !!")
        elif vote == 2:
            nm2_votes=+1
            print(nominee2,"Thanks yoi to give your important to them !!")
        elif vote >2:
            print("check your pressed key !!")
        else:
            print("you are not a voter OR you have already voted")
