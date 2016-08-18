#include<iostream.h>
#include<conio.h>
#include<stdlib.h>

const int s=10;
int a[s];
int f=-1;
int r=-1;
void enqueue(int);
void dequeue();
void print();

void main()
{
 clrscr();
 int x,c;
 while(1)
 {
   clrscr();
   cout<<"Enter your choice\n";
   cout<<"1.Enqueue an element\n";
   cout<<"2.Dequeue an element\n";
   cout<<"3.Print the list\n";
   cout<<"4.Exit\n";
   cin>>c;
   switch(c)
   {
      case 1:
	     {
	       cout<<"Enter an element\n";
	       cin>>x;
	       enqueue(x);
	       break;
	     }
      case 2:
	     {
	       dequeue();
	       break;
	     }
      case 3:
	     {
	       print();
	       getch();
	       break;
	     }
      case 4:
	     {
		exit(1);
		break;
	     }
     default:
	     {
	       cout<<"Invalid statement\n";
	       break;
	     }

    }
  }
}

void enqueue(int x)
{

   if(((r+1)%s)==f)
   {
     cout<<"Queue is full\n";
     getch();
     return;
   }
   else if(f==-1&&r==-1)
   f=r=0;
   else
   r=(r+1)%s;
   a[r]=x;
}

void dequeue()
{
  if(f==-1&&r==-1)
  {
   cout<<"Queue is empty\n";
   getch();
   return;
  }
  else if(f==r)
  {
     f=r=-1;
     cout<<"Queue is empty now\n";
     getch();
     return;
  }
  else f=(f+1)%s;
}

void print()
{
 int i;
 cout<<"front element-> "<<a[f]<<"\n";
 cout<<"rear element-> "<<a[r]<<"\n";
 cout<<"List is: \n";
 for(i=f;i!=r;i=((i+1)%s))
   {
      cout<<a[i]<<" ";
   }
 cout<<a[r]<<"\n";
}