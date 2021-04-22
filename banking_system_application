#include<stdio.h>
#include<stdlib.h>
#include<string.h>

long long int accountNumber=88258342160,accountIdNum=67890;


struct bank{
    char name[1001],dob[1001],password[1001],gender;
    long long int mobileNumber,aadharNumber,age,balance;
}accountId[1001];


void createAccount(){
    printf("\nEnter account holder name:\n");
    scanf("%s",accountId[accountIdNum-67889].name);
    printf("Enter age:\n");
    scanf("%lld",&accountId[accountIdNum-67889].age);
    printf("Enter DOB:\n");
    scanf("%s",accountId[accountIdNum-67889].dob);
    printf("Enter gender:\n");
    scanf(" %c",&accountId[accountIdNum-67889].gender);
    printf("Enter aadhar number:\n");
    scanf("%lld",&accountId[accountIdNum-67889].aadharNumber);
    printf("Enter mobile number:\n");
    scanf("%lld",&accountId[accountIdNum-67889].mobileNumber);
    accountId[accountIdNum-67889].balance=0;
    printf("Create your password:\n");
    scanf("%s",accountId[accountIdNum-67889].password);
    printf("\n***-----Account created successfully-----***\n\nYour Account Number is : %lld\nYour Customer ID is : %lld\n\n",accountNumber++,accountIdNum++);
}

void viewDetails(long long int id){
    printf("\nYour account details are:\n\nName : %s\nAge : %lld\nDOB : %s\nGender : %c\nAadhar Number : %lld\nMobile Number : %lld\nBank Balance : %.2f\n\n",accountId[id-67889].name,accountId[id-67889].age,accountId[id-67889].dob,accountId[id-67889].gender,accountId[id-67889].aadharNumber,accountId[id-67889].mobileNumber,(double)accountId[id-67889].balance);
}

void viewBalance(long long int id){
  printf("\nYour account balance is %.2f",(double)accountId[id-67889].balance);
}

void amountTransfer(long long int id){
  char pass[1001];
  long long int id2,amountSend;
  printf("Enter your valid password:\n");
  scanf("%s",pass);
  while(strcmp(accountId[id-67889].password,pass)!=0){
      printf("Enter your valid password:\n");
      scanf("%s",pass);
  }
  printf("Enter the customer id of the person to sent amount:\n");
  scanf("%lld",&id2);
  printf("Enter the amount to be sent:\n");
  scanf("%lld",&amountSend);
  while(amountSend>accountId[id-67889].balance){
    printf("Your account balance is %.2f\n\n",(double)accountId[id-67889].balance);
      printf("So enter the valid amount to be sent:\n");
      scanf("%lld",&amountSend);
  }
  accountId[id-67889].balance=accountId[id-67889].balance-amountSend;
  accountId[id2-67889].balance=accountId[id2-67889].balance+amountSend;
  printf("Transaction Successfull\n\nNow your account balance is %.2f\n\n",(double)accountId[id-67889].balance);
}

void editProfile(long long int id){
  char pass[1001],ch,name[1001],gender,dob[1001],ind[1001];
  long long int age,aadhar,mobile;
  printf("Enter your valid password:\n");
  scanf("%s",pass);
  while(strcmp(accountId[id-67889].password,pass)!=0){
      printf("\nPlease enter your valid password again:\n");
      scanf("%s",pass);
  }
  printf("Enter 'n' to change your name\nEnter 'a' to change the age\nEnter 'd' to change the dob\nEnter 'g' to change the gender\nEnter 'p' to change the password\nEnter 'm' to change the mobile number\nEnter 'c' to change the aadhar number\n\n");
scanf(" %c",&ch);
switch(ch){
  case 'n':
    printf("Enter name:\n");
    scanf("%s",name);
    printf("\nAre you sure want to change your profile? Enter yes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)strcpy(accountId[id-67889].name,name);
    printf("Edited Successfully");
    break;
  case 'a':
    printf("Enter age:\n");
    scanf("%lld",&age);
    printf("Are you sure want to change your profile?\nyes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)accountId[id-67889].age=age;
    printf("Edited Successfully");
    break;
  case 'd':
    printf("Enter DOB:\n");
    scanf("%s",dob);
    printf("Are you sure want to change your profile?\nyes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)strcpy(accountId[id-67889].dob,dob);
    printf("Edited Successfully");
    break;
  case 'g':
    printf("Enter gender:\n");
    scanf("%c ",&gender);
    printf("Are you sure want to change your profile?\nyes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)accountId[id-67889].gender=gender;
    printf("Edited Successfully");
    break;
  case 'p':
    printf("Enter new password:\n");
    scanf("%s",pass);
    printf("Are you sure want to change your profile?\nyes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)strcpy(accountId[id-67889].password,pass);
    printf("Edited Successfully");
    break;
  case 'm':
    printf("Enter mobile number:\n");
    scanf("%lld",&mobile);
    printf("Are you sure want to change your profile?\nyes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)accountId[id-67889].mobileNumber=mobile;
    printf("Edited Successfully");
    break;
  case 'c':
    printf("Enter aadhar number:\n");
    scanf("%lld",&aadhar);
    printf("Are you sure want to change your profile?\nyes or no\n");
    scanf("%s",ind);
    if(strcmp(ind,"yes")==0)accountId[id-67889].aadharNumber=aadhar;
    printf("Edited Successfully");
    break;
  default:
    break;
}
}

int main()
{
char ch,pass[1001];
long long int id,amountCredit,amountDebit;
do{
    printf("\n\n\n\t*****\tWELCOME ! How can I help you?\t*****\n\n-> Enter '1' to create new account\n-> Enter '2' to view profile\n-> Enter '3' to view account balance\n-> Enter '4' to transfer amount\n-> Enter '5' for credit process\n-> Enter '6' for debit process\n-> Enter '7' to edit your account\n-> Enter any other number to exit\n\n");
    scanf(" %c",&ch);
    switch(ch){
        case '1':
            createAccount();
            break;
        case '2':
            printf("\nEnter your Customer Id:\n");
            scanf("%lld",&id);
            viewDetails(id);
            break;
        case '3':
          printf("\nEnter your Customer Id:\n");
          scanf("%lld",&id);
          viewBalance(id);
          break;
        case '4':
          printf("\nEnter your customer Id:\n");
          scanf("%lld",&id);
          amountTransfer(id);
          break;
        case '5':
          printf("\nEnter your customer Id:\n");
          scanf("%lld",&id);
          printf("Enter your valid password:\n");
          scanf("%s",pass);
          while(strcmp(accountId[id-67889].password,pass)!=0){
              printf("\nPlease enter your valid password again:\n");
              scanf("%s",pass);
          }
          printf( "\nEnter the amount to credit\n");
          scanf("%lld",&amountCredit);
          accountId[id-67889].balance=accountId[id-67889].balance+amountCredit;
          printf("\nCredited Successfully\n\nNow your account balance is %.2f\n\n",(double)accountId[id-67889].balance);
          break;
        case '6':
          printf("\nEnter your customer Id:\n");
          scanf("%lld",&id);
          printf("Enter your valid password:\n");
          scanf("%s",pass);
          while(strcmp(accountId[id-67889].password,pass)!=0){
              printf("\nPlease enter your valid password again:\n");
              scanf("%s",pass);
          }
          printf( "Enter the amount to debit\n");
          scanf("%lld",&amountDebit);
          accountId[id-67889].balance=accountId[id-67889].balance-amountDebit;
          printf("\nDebited Successfully\n\nNow your account balance is %.2f\n\n",(double)accountId[id-67889].balance);
          break;
        case '7':
          printf("\nEnter your customer Id:\n");
          scanf("%lld",&id);
          editProfile(id);
          break;
        default:
            printf("\nThank you...Welcome again\n");
            exit(1);
            break;
    }
}while(1);
}
