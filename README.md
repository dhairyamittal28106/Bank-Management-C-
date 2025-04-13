#include<iostream>
using namespace std ;
class bank_account{
	string name ,account_type; 
	int account_no ,balance_amount ,deposit, withdraw , netbalance;
	public :
	void getdata() {
		cout<<"Enter account holder name :"<< name << endl;
		cin>> name;
		cout<<"Enter account type :"<< endl;
		cin>> account_type;
		cout<<"Enter account number :"<< endl;
		cin>> account_no;
		cout<<"Enter balance amount :"<< endl;
		cin>> balance_amount;
	}
	void transactions() {
		cout<<"Enter balance amount :"<< balance_amount << endl;
		cout<<"Press 1 to DEPOSIT :"<< "\nPress 2 to WITHDRAW :" << "\nPress 3 for both :"<<endl;
		int a;
		cin>> a;
		if(a==1)
		{
		 cout<<"enter deposit amount :" << endl;
		 cin>> deposit ;
		netbalance = balance_amount + deposit ;
		}
		else if (a==2){
				cout<<"enter withdraw amount :" << endl;
		        cin>> withdraw ;
		        netbalance = balance_amount - withdraw;
		}
		else if (a==3)
		{
			cout<<"enter deposit amount :" << endl;
		    cin>> deposit ;
			cout<<"enter withdraw amount :" << endl;
			cin>> withdraw ;
			netbalance = balance_amount + deposit - withdraw; 
		}
		
		else {
			cout<<"Invalid " << endl;
		}
	}	
	void display(){
		cout<<"-----------------------"<< endl;
		cout<<"Account Holder Name :"<< name<< endl;
		cout<<"Balance:"<< netbalance<< endl;
	    cout<<"-----------------------"<< endl;	
	
	}
};
   int main() {
   	string choice = "Y" ;
   	while (choice == "y" || choice == "Y"){
   		bank_account a1;
   		a1.getdata();
   		a1.transactions();
   		a1.display();
   		cout<<"Do you want to continue (y/n) ? " << endl;
   		cin>> choice ;
	   }
	   cout<< "Thank You  ! " << endl;
	   return 0;
   }
