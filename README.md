#include<iostream>
#include<iomanip>
#include<conio.h>
#include<fstream>
#include<cstring>
#include<windows.h>

void menu();
void pascode();
void cpascodde();
using namespace std;

 class one  
  {
 	public :
 	virtual void get()=0;
 	virtual void show()=0;
  };
 class info : public one 
 { 
   public: ;
   char name[50],time[50];
   int num,age;
   void get()
   {
   	system ("clas");
   	cin.sync();
   	cout<<"\n Enter the patient name = ";
   	cin.getline(name,50);
   	cout<<"\n Enter the appontment time = ";
   	cin.getline(time,50);
   	cout<<"\n Enter the patient age = ";
   	cin>>age;
   	cout<<"\n Enter the patient NO = ";
   	cin>>num;
    
  	
   }
   void show()
   {
   	cout<<"\n  Name = "<< name;
   	cout<<"\n age ="<< age;
   	cout<<"\n NO = "<< num;
	cout<<"\n Time ="<<time;
	   }
  	
 };
 class Rana : public info {
 	public : ;
 	info a1;
 	void get(){
 		system("cls");
 		ofstream out("Rana.txt",ios::app| ios:: binary);
 		a1.get();
 		out.write((char*)&a1,sizeof(info));
 		out.close();
 		cout<<"Your Entery has been saved ";
 		getch();
 		menu();
	 }
	 
 void show(){
 
  ifstream in("Rana.txt");
 if(in==NULL){
 	cout<<"\n \n NO data in files ";
	cout<<"\n \n \t \t Press any key to continue";
	getch();
	menu();
	 }
	 else {
	 	while(!in.eof()){
	 		in.read((char*)&a1,sizeof(a1));
	 		a1.show();
		 }
		 in.close();
		 getch();
		 menu();
	 }
	 
 }		
 };
 class ibrahim : public info{
 	
 	public:
 	info a1;
 	void get(){
 		system("cls");
 		ofstream out("ibrahim.txt",ios::app| ios:: binary);
 		a1.get();
 		out.write((char*)&a1,sizeof(info));
 		out.close();
 		menu();
	 }
	 
 void show(){
 
 ifstream in ("ibrahim.txt");
 if(in==NULL){
 	cout<<"\n \n NO data in files ";
	cout<<"\n \n \t \t Press any key to continue";
	getch();
	menu();
	 }else {
	 	while(!in.eof()){
	 		in.read((char*)&a1,sizeof(a1));
	 		a1.show();
		 }
		 in.close();
		 getch();
		 menu();
 }
 };
 class ali : public info{
 	public:
 	info a1;
 	void get(){
 		system("cls");
 		ofstream out("ali.txt",ios::app| ios:: binary);
 		a1.get();
 		out.write((char*)&a1,sizeof(info));
 		out.close();
 		menu();
	 }
	 
 void show(){
 
 ifstream in ("ali.txt");
 if(in==NULL){
 	cout<<"\n \n NO data in files ";
	cout<<"\n \n \t \t Press any key to continue";
	getch();
	menu();
	 }else {
	 	while(!in.eof()){
	 		in.read((char*)&a1,sizeof(a1));
	 		a1.show();
		 }
		 in.close();
		 getch();
		 menu();
 }
 };
 
 class stuf : public one {
 	public:
 		char all[999];
 		char name[50],age[50],sal[30],pos[20];;
void get()
{
	ofstream out("stuff.txt",ios::app);
	{
	
 	system ("cls");
   	cin.sync();
   	cout<<"\nEnter Name = ";
   	cin.getline(name,50);
   	cout<<"\n Enter Age = ";
   	cin.getline(age,50);
   	cout<<"\n Enter Sallary = ";
   	cin.getline(sal,30);
   	cout<<"\n Enter Working Position = ";
   	cin.getline(pos,20);
   	
                                 }  
								    
    out<<"\nName ="<<name<<"\n Age ="<<age<<"\n Sallary = "<<sal<<"\n Working Position\n"<<pos;
    out.close();
    cout<<"\n \n Your Information has been saved :\n\t\t\t Press any key to continue  ";
    getch();
    menu();
}
};
 };
 };
 
 
