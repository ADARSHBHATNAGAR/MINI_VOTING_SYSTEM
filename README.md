# MINI_VOTING_SYSTEM

#include<stdio.h>
  int votecount1=0, votecount2=0, votecount3=0, votecount4=0, spoiledvotes=0;
  char A[]={"CANDIDATE1"};
	char B[]={"CANDIDATE2"};
	char C[]={"CANDIDATE3"};
	char D[]={"CANDIDATE4"};
	char E[]={"SPOILEDVOTES"};
	void leadingcandidate(){
		
		if(votecount1>(votecount2 && votecount3 && votecount4)){
			printf("Leading Candidate --> %s", "CANDIDATE1");
		}
		else if(votecount2>(votecount1 && votecount3 && votecount4)){
			printf("Leading Candidate --> %s", "CANDIDATE2");
		}
		else if(votecount3>(votecount2 && votecount1 && votecount4)){
			printf("Leading Candidate --> %s", "CANDIDATE3");
		}
		else if(votecount4>(votecount2 && votecount3 && votecount1)){
			printf("Leading Candidate --> %s", "CANDIDATE4");
		}
		
		
	}
void votescount(){
	printf("\t\t\t\t\t |***VOTING STATISTICS***|");
	  printf("%s ---> %d", "CANDIDATE1",votecount1);
		  printf("%s ---> %d", "CANDIDATE2",votecount2);
			  printf("%s ---> %d", "CANDIDATE3",votecount3);
				  printf("%s ---> %d", "CANDIDATE4",votecount4);
				
				    
				    
	
}
void castvote(){
	
	int CHOSEN;
	
	printf("\t\t\t>>>>NAME OF CANDIDATES AND THEIR SELECTION MARKS<<<<\n");
	printf("1. %s --> 1\n", "CANDIDATE1");
	printf("2. %s --> 2\n", "CANDIDATE2");
	printf("3. %s --> 3\n", "CANDIDATE3");
	printf("4. %s --> 4\n", "CANDIDATE4");
	
	
	printf("Choose (1-4)\n");
	scanf("%d", &CHOSEN);
	
	if(CHOSEN==1){
			votecount1++;
	}else if(CHOSEN==2){
		votecount2++;
	}else if(CHOSEN==3){
		votecount3++;
	}else if(CHOSEN==4){
		votecount4++;
	}else if(CHOSEN==5){
		spoiledvotes++;
	}else {
	
		printf("Error! Wrong choice please retry....!");
	}
	
	printf("Thanks for vote!");
	
	
	
	
	
	
	
}
int main(){
	int choice;
	
	do{
	printf("######## WELCOME TO ELECTION VOTING 2022 ########");
	printf("\n 1. CAST YOUR VOTE\n");
	printf("\n 2. FIND VOTE COUNT\n");
	printf("\n 3. FIND LEADING CANDIDATE\n");
	printf("\n 4. EXIT\n");
	
	printf("\n\nEnter your choice\n");
	scanf("%d", &choice);
	
	switch(choice){
		case 1 : castvote(); break ;
		case 2 : votescount(); break ;
		case 3 : leadingcandidate(); break ;
		default : printf("Wrong Choice\n"); break;
	}}while(choice!=4);
	
	return 0;
	
	
	
	
}
