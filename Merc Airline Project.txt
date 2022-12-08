#include <iostream>
#include <conio.h>
#include <windows.h>
#include <cstdlib>
#include <string>
#include <stdlib.h>
#include <stdio.h>
#include <climits>
#include <sstream>
#include <iomanip>

using namespace std;

HANDLE console = GetStdHandle(STD_OUTPUT_HANDLE);
COORD CursorPosition;

void gotoXY(int,int); 

void SetColor(int value){
    SetConsoleTextAttribute(GetStdHandle(STD_OUTPUT_HANDLE),  value);
}
void ShowConsoleCursor(bool showFlag)
{
    HANDLE out = GetStdHandle(STD_OUTPUT_HANDLE);

    CONSOLE_CURSOR_INFO     cursorInfo;

    GetConsoleCursorInfo(out, &cursorInfo);
    cursorInfo.bVisible = showFlag; // set the cursor visibility
    SetConsoleCursorInfo(out, &cursorInfo);
}
int main()
{
    ShowConsoleCursor(false);
	
	Box_Design:
		int b_d, b_d_x = 2, b_d_y = 3;
		char b_box = 219;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		 
		 gotoXY(4,4); cout<<"WELCOME TO MERC AIRLINES";
		
		
		 
		 b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,6); cout << b_box;
			b_d_x++;	
	}
		Sleep(500);
	
		gotoXY(9,8); cout<<"Developed By";
		Sleep(500);
	
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,10); cout << b_box;
			b_d_x++;
		}
		gotoXY(9,12); cout<<"Projext Diva";
		 Sleep(500);
		 
		 b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,14); cout << b_box;
			b_d_x++;
		}
		gotoXY(9,16);cout<<"Michael Vargas";
		gotoXY(9,17);cout<<"Julian Monleon";
		gotoXY(9,18);cout<<"Patrick Etesam";
		gotoXY(9,19);cout<<"Hans Villanueva";
		gotoXY(9,20);cout<<"Gie Arellano";
		gotoXY(9,21);cout<<"Justin Barcos";
		
		Sleep(2500);
		system("cls");
	
	Box_17:
		bool run_start = true;
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
			
		gotoXY(4,4); cout << "WELCOME TO MERC AIRLINES";
		
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,6); cout << b_box;
			b_d_x++;
		}
		
		gotoXY(7,8); cout << "WOULD YOU LIKE TO:";
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,10); cout << b_box;
			b_d_x++;
		}
		
		gotoXY(12,12); cout << "Book a flight";
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,14); cout << b_box;
			b_d_x++;
		}
		
		gotoXY(12,16); cout << "Exit the program";
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,18); cout << b_box;
			b_d_x++;
		}
		
		b_d_y = 10;
		
		while(b_d_y < 19){
			gotoXY(10,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		gotoXY(4,20); cout << "Press up and down to pick";
		gotoXY(15,21); cout << "&";
		gotoXY(4,22); cout << "Press enter to continue ";
		
	
	Start_Choice:
		int st_y = 2, st_state = 0;
		bool st_p = true;
		do{
			system("pause>nul");
			
			if(GetAsyncKeyState(VK_UP)){
				gotoXY(4,16); cout << "     ";
				SetColor(10);
				gotoXY(12,16); cout << "Exit the program";
				st_state--;
				goto st_check_state;
			}
			
			if(GetAsyncKeyState(VK_DOWN)){
				gotoXY(4,12); cout << "     ";
				SetColor(10);
				gotoXY(12,12); cout << "Book A flight";
				st_state++;
				goto st_check_state;
			}
			
			if(GetAsyncKeyState(VK_RETURN)){
					switch(st_state){
						case 0:
							goto st_check_state;
							break;
						case 1:
							st_booking:
								system("cls");
								st_p = false;
							break;
								
						case 2:
							system("pause>nul");
							system("cls");
							return 0;
					}
			}
			
			if(st_p){
			}
			else{
				break;
			}
			
			st_check_state:
				switch(st_state){
					case -1:
						st_state += 2;
						goto st_check_state;
						break;
					case 0:
						st_state++;
						goto st_check_state;
						break;
					case 1:
						SetColor(12);
						gotoXY(4,12); cout << b_box << b_box << b_box << b_box << b_box;
						gotoXY(12,12); cout << "Book A flight";
						SetColor(10);
						break;
					case 2:
						SetColor(12);
						gotoXY(4,16); cout << b_box << b_box << b_box << b_box << b_box;
						gotoXY(12,16); cout << "Exit the program";
						SetColor(10);
						break;
					case 3:
						st_y --;
						st_state--;
						break;
				}
			
		}while(st_p);
		
	box_2:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,15); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
	Customer_Info_Gathering:
		
		
		gotoXY(10,3); cout << "MERC AIRLINE";
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
		
		gotoXY(4,6); cout << "Please fill in your";
		gotoXY(4,7); cout << "booker's information";
		
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,9); cout << b_box;
			b_d_x++;
		}
		
		CST_Info_gath:
  		  ShowConsoleCursor(true);
			int cst_age, cst_name_s;
			
			string cst_age_s, cst_name;
			SetColor(12);
			gotoXY(4,11); cout << "Name:";
			SetColor(10);
			gotoXY(4,13); cout << "Age:";
			
		cst_name_c:
			gotoXY(9,11); getline(cin,cst_name);
			
			cst_n_check_emp:	
				while(cst_name.empty()){
					gotoXY(9,11); cout << "\t\t";
					
					gotoXY(9,11); getline(cin,cst_name);
				}
				
			cst_n_check_no:
				while(string::npos != cst_name.find_first_of("0123456789=+'_><.,/?\\|][{}]*!@#$%&*(_)")){
					gotoXY(9,11); cout << "\t\t";
					gotoXY(9,11); getline(cin,cst_name);
					
					if(cst_name.empty()){
						goto cst_n_check_emp;
					}
				}
			
			SetColor(12);
			gotoXY(4,13); cout << "Age:";
			SetColor(10);
			gotoXY(4,11); cout << "Name:";
				
		cst_age_c:
			gotoXY(8,13); getline(cin,cst_age_s);
			
			stringstream cst_a (cst_age_s);
			cst_a >> cst_age;
			
			cst_a_check_emp:
				while(cst_age_s.empty()){
					SetColor(10);							
					
					gotoXY(8,13); cout << "\t\t";
					gotoXY(8,13); getline(cin,cst_age_s);
							
					stringstream cst_a (cst_age_s);
					cst_a >> cst_age;
					
					gotoXY(4,21); cout << "\t\t\t";
					gotoXY(4,22); cout << "\t\t\t";
				}
			
			cst_a_check_let:
				while(string::npos != cst_age_s.find_first_of("QWERTYUIOPASDFGHJKLXCVBNMZabcdefghijklmnopqrstuvwxyz!@#$$%&*()_-=+*/.></?'\":;\\")){
					SetColor(10);
				
					gotoXY(8,13); cout << "\t\t";
					gotoXY(8,13); getline(cin,cst_age_s);
					
					if(cst_age_s.empty()){
						goto cst_a_check_emp;
					}
					
				}
	
	cst_undo:
		ShowConsoleCursor(false);
		
		int cst_undo_state = 0;
		bool cst_undo_d=true;
		
		gotoXY(4,17); cout << "Is all of this correct?";
		gotoXY(12,19); cout << "[YES]";
		gotoXY(12,21); cout << "[NO]";
		
		while(cst_undo_d){
		
			system("pause>nul");
			
			if(GetAsyncKeyState(VK_UP)){
				cst_undo_state--;
				goto cst_undo_sub;
			}
			if(GetAsyncKeyState(VK_DOWN)){
				cst_undo_state++;
				goto cst_undo_sub;
			}
			if(GetAsyncKeyState(VK_LEFT)){
				goto cst_undo_sub;
			}
			if(GetAsyncKeyState(VK_RIGHT)){
				goto cst_undo_sub;
			}
			if(GetAsyncKeyState(VK_RETURN)){
				switch(cst_undo_state){
					case 1:
						cst_undo_d = false;
						break;
					case 2:
						goto box_2;
						break;
				}
			}
			
			cst_undo_sub:
				switch(cst_undo_state){
					case 0:
						cst_undo_state = 2;
						goto cst_undo_sub;
						break;
						
					case 1:
						SetColor(12);
						gotoXY(10,19); cout << "[  YES  ]";
						SetColor(10);
						gotoXY(10,21); cout << "  [NO]   ";
						break;
						
					case 2:
						SetColor(12);
						gotoXY(10,21); cout << "[  NO   ]";
						SetColor(10);
						gotoXY(10,19); cout << "  [YES]   ";
						break;
					default:
						cst_undo_state = 1;
						goto cst_undo_sub;
						break;
				}
		}
		
		
	box_4:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,20); cout << b_box;
			b_d_x++;
		}
		
	Destination_selection_Text:
		
		ShowCursor(false);
		
		bool d_sel = true;
		
		gotoXY(10,3); cout << "MERC AIRLINE";
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			gotoXY(b_d_x,8); cout << b_box;
			gotoXY(b_d_x,10); cout << b_box;
			gotoXY(b_d_x,15); cout << b_box;
			b_d_x++;
		}
		
		b_d_y = 4;
		
		while(b_d_y < 9){
			gotoXY(8,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(24,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_y = 8;
		
		while(b_d_y < 20){
			gotoXY(13,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
	Destination_selection:
		
		SetColor(12);
		gotoXY(13,6); cout << "Batanes";
		
		gotoXY(4,6); cout << "<==";
		
		gotoXY(26,6); cout << "==>";
		SetColor(10);
		
		gotoXY(5,9); cout << "Class";
		
		gotoXY(19,9); cout << "Prices";
		
		gotoXY(4,12); cout << "Private";
		gotoXY(4,13); cout << " Class";
		
		gotoXY(4,17); cout << "Business";
		gotoXY(4,18); cout << " Class";
		
		gotoXY(16,12); cout << "8,650 PHP ";
		gotoXY(16,13); cout << "Per Person";
		
		gotoXY(16,17); cout << "15,500 PHP";
		gotoXY(16,18); cout << "Per Person";
		
		gotoXY(4,21); cout << "Arrow Keys -  Navigation";
		gotoXY(4,22); cout << "  Enter    - Confirmation";
		gotoXY(4,23); cout << "Backspace  - Undo / Back";
	
		
		int d_sel_state = 1,
			price_p,
			price_b;
			
		string price_p_s,
			   price_b_s,
			   string_dest[10] = {"mike","Batanes","Bacolod","Palawan","Davao","Malaysia","Indonesia","Singapore","South Korea","Japan"};
		
		
		
		while(d_sel){
			system("pause>nul");
			
			if(GetAsyncKeyState(VK_UP)){
				goto sub_d_sel;
			}
			if(GetAsyncKeyState(VK_DOWN)){
				goto sub_d_sel;
			}
			if(GetAsyncKeyState(VK_LEFT)){
				gotoXY(10,6); cout <<  "\t        ";
				gotoXY(16,12); cout << "\t      ";
				gotoXY(16,17); cout << "\t      ";
				d_sel_state--;
				goto sub_d_sel;
			}
			if(GetAsyncKeyState(VK_RIGHT)){
				gotoXY(10,6); cout <<  "\t        ";
				gotoXY(16,12); cout << "\t      ";
				gotoXY(16,17); cout << "\t      ";
				d_sel_state++;
				goto sub_d_sel;
			}
			if(GetAsyncKeyState(VK_UP)){
				goto sub_d_sel;
			}
			if(GetAsyncKeyState(VK_DOWN)){
				goto sub_d_sel;
			}
			if(GetAsyncKeyState(VK_RETURN)){
				switch(d_sel_state){
					case 1:
						price_p = 8650;
						price_b = 15500;
						price_p_s = "8,650 PHP";
						price_b_s = "15,500 PHP";
						d_sel = false;
						break;
					case 2:
						price_p = 4543;
						price_b = 9500;
						price_p_s = "4,543 PHP";
						price_b_s = "9,500 PHP";
						d_sel = false;
						break;
					case 3:
						price_p = 5882;
						price_b = 13200;
						price_p_s = "5,882 PHP";
						price_b_s = "13,200 PHP";
						d_sel = false;
						break;
					case 4:
						price_p = 4096;
						price_b = 9230;
						price_p_s = "4,096 PHP";
						price_b_s = "9,230 PHP";
						d_sel = false;
						break;
					case 5:
						price_p = 6199;
						price_b = 12150;
						price_p_s = "6,199 PHP";
						price_b_s = "12,150 PHP";
						d_sel = false;
						break;
					case 6:
						price_p = 5699;
						price_b = 10850;
						price_p_s = "5,699 PHP";
						price_b_s = "10,850 PHP";
						d_sel = false;
						break;
					case 7:
						price_p = 6899;
						price_b = 13110;
						price_p_s = "6,899 PHP";
						price_b_s = "13,110 PHP";
						d_sel = false;
						break;
					case 8:
						price_p = 12500;
						price_b = 23850;
						price_p_s = "12,500 PHP";
						price_b_s = "23,850 PHP";
						d_sel = false;
						break;
					case 9:
						price_p = 24800;
						price_b = 31450;
						price_p_s = "24,800 PHP";
						price_b_s = "31,450 PHP";
						d_sel = false;
						break;
				}
			}
			
			sub_d_sel:
				switch(d_sel_state){
					case 0:
						d_sel_state = 9;
						goto sub_d_sel;
						break;
					case 1:
						SetColor(12);
						gotoXY(13,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "8,650 PHP";
						gotoXY(16,17); cout << "15,500 PHP";
						break;
					case 2:
						SetColor(12);
						gotoXY(13,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "4,543 PHP";
						gotoXY(16,17); cout << "9,500 PHP";
						break;
					case 3:
						SetColor(12);
						gotoXY(13,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "5,882 PHP";
						gotoXY(16,17); cout << "13,200 PHP";
						break;
					case 4:
						SetColor(12);
						gotoXY(14,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "4,096 PHP";
						gotoXY(16,17); cout << "9,230 PHP";
						break;
					case 5:
						SetColor(12);
						gotoXY(12,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "6,199 PHP";
						gotoXY(16,17); cout << "12,150 PHP";
						break;
					case 6:
						SetColor(12);
						gotoXY(12,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "5,699 PHP";
						gotoXY(16,17); cout << "10,850 PHP";
						break;							
					case 7:			
						SetColor(12);						
						gotoXY(12,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "6.899 PHP";
						gotoXY(16,17); cout << "13,110 PHP";
						break;
					case 8:
						SetColor(12);
						gotoXY(11,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "12,500 PHP";
						gotoXY(16,17); cout << "23,850 PHP";
						break;
					case 9:
						SetColor(12);
						gotoXY(14,6); cout <<  string_dest[d_sel_state];
						SetColor(10);
						gotoXY(16,12); cout << "24,800 PHP";
						gotoXY(16,17); cout << "31,450 PHP";
						break;
					case 10:
						d_sel_state = 1;
						goto sub_d_sel;
						break;
				}
		}
		
		//Will you do this for me?
		
		switch(d_sel_state){
					case 1:
						SetColor(10);
						gotoXY(13,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 2:
						SetColor(10);
						gotoXY(13,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 3:
						SetColor(10);
						gotoXY(13,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 4:
						SetColor(10);
						gotoXY(14,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 5:
						SetColor(10);
						gotoXY(12,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 6:
						SetColor(10);
						gotoXY(12,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;							
					case 7:			
						SetColor(10);						
						gotoXY(12,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 8:
						SetColor(10);
						gotoXY(11,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						break;
					case 9:
						SetColor(10);
						gotoXY(14,6); cout <<  string_dest[d_sel_state];
						gotoXY(4,6); cout << "<==";
						
						gotoXY(26,6); cout << "==>";
						
						break;
		}
		
	Class_Selection:
		int class_sel_state = 0, price;
		bool class_sel = true, priv = false, buss = false;
		string price_sp;
		while(class_sel){
			
			system("pause>nul");
			
			if(GetAsyncKeyState(VK_UP)){
				class_sel_state--;
				goto class_sel_sub;
			}
			if(GetAsyncKeyState(VK_DOWN)){
				class_sel_state++;
				goto class_sel_sub;
			}
			if(GetAsyncKeyState(VK_LEFT)){
				goto class_sel_sub;
			}
			if(GetAsyncKeyState(VK_RIGHT)){
				goto class_sel_sub;
			}
			
			if(GetAsyncKeyState(VK_BACK)){
				SetColor(10);
				class_sel = false;
				d_sel = true;
				gotoXY(10,6); cout <<  "\t        ";
				goto Destination_selection;
			}
			
			if(GetAsyncKeyState(VK_RETURN)){
				switch(class_sel_state){
					case 1:
						priv = true;
						price = price_p;
						price_sp = price_p_s;
						class_sel = false;
						break;
					case 2:
						buss = true;
						price = price_b;
						price_sp = price_b_s;
						class_sel = false;
						break;
				}
			}
			
			class_sel_sub:
				switch(class_sel_state){
					case 0:
						class_sel_state = 2;
						goto class_sel_sub;
						break;
					case 1:
						SetColor(12);
						gotoXY(16,12); cout << price_p_s;
						
						gotoXY(4,12); cout << "Private";
						
						gotoXY(4,13); cout << " Class";
						
						gotoXY(16,13); cout << "Per Person";
						SetColor(10);
						gotoXY(16,17); cout << price_b_s;
						gotoXY(4,17); cout << "Business";
						gotoXY(4,18); cout << " Class";
						gotoXY(16,18); cout << "Per Person";
						break;
					case 2:
						SetColor(12);
						gotoXY(16,17); cout << price_b_s;
					
						gotoXY(4,17); cout << "Business";
						
						gotoXY(4,18); cout << " Class";
						
						gotoXY(16,18); cout << "Per Person";
						SetColor(10);
						gotoXY(16,12); cout << price_p_s;
						gotoXY(4,12); cout << "Private";
						gotoXY(4,13); cout << " Class";
						gotoXY(16,13); cout << "Per Person";
						break;
					default:
						class_sel_state = 1;
						goto class_sel_sub;
						break;
				}
		}
		
		system("cls");
		
	box_11:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
				
		b_d_y = 2;
			
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
				//Sleep(50);
		}
			
		b_d_x = 2;
			
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
			
		while(b_d_x <= 30){
			gotoXY(b_d_x,20); cout << b_box;
			b_d_x++;
		}
			
		b_d_x = 2;
				
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
				
		gotoXY(10,3); cout << "MERC AIRLINE";
			
		pass_Rountrip:
			bool round_trip = false;
			cst_undo_d=true;
			
			cst_undo_state = 0;
			
			gotoXY(5,6); cout << "Is this a RoundTrip?";
			gotoXY(12,9); cout << "[YES]";
			gotoXY(12,11); cout << "[NO]";
				
			while(cst_undo_d){
				
				system("pause>nul");
					
				if(GetAsyncKeyState(VK_UP)){
					cst_undo_state--;
					goto cst_undo_sub4;
				}
				if(GetAsyncKeyState(VK_DOWN)){
					cst_undo_state++;
					goto cst_undo_sub4;
				}
				if(GetAsyncKeyState(VK_LEFT)){
					goto cst_undo_sub4;
				}
				if(GetAsyncKeyState(VK_RIGHT)){
					goto cst_undo_sub4;
				}
				if(GetAsyncKeyState(VK_RETURN)){
					switch(cst_undo_state){
						case 1:
							cst_undo_d = false;
							round_trip = true;
							
							break;
						case 2:
							cst_undo_d = false;
							break;
					}
				}
					
				cst_undo_sub4:
					switch(cst_undo_state){
						case 0:
							cst_undo_state = 2;
							goto cst_undo_sub4;
							break;
							
						case 1:
							SetColor(12);
							gotoXY(10,9); cout << "[  YES  ]";
							SetColor(10);
							gotoXY(10,11); cout << "  [NO]   ";
							break;
							
						case 2:
							SetColor(12);
							gotoXY(10,11); cout << "[  NO   ]";
							SetColor(10);
							gotoXY(10,9); cout << "  [YES]   ";
							break;
						default:
							cst_undo_state = 1;
							goto cst_undo_sub4;
							break;
					}
		}
		
	
	box_5:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,20); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
		
		gotoXY(10,3); cout << "MERC AIRLINE";
		
	Pass_size:
		int pass_size;
		string pass_size_s;
		
		ShowConsoleCursor(true);
		
		gotoXY(10,8); cout <<   "Please Enter";
		gotoXY(7,9); cout << "How many passenger:";
		gotoXY(14,13); cout << ":";
		gotoXY(15,13); getline(cin, pass_size_s);
		
		stringstream misf (pass_size_s);
		misf >> pass_size;
		
		pass_size_emp:
			while(pass_size_s.empty()){	
				gotoXY(15,13); getline(cin, pass_size_s);
				
				stringstream misf (pass_size_s);
				misf >> pass_size;
			}
			
		pass_size_let:
			while(string::npos != pass_size_s.find_first_of("qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM{}|[];'<>,./?@#$%&*()`~^\\\"" )){
				gotoXY(15,13); cout << "\t             ";
				gotoXY(15,13); getline(cin, pass_size_s);
				
				stringstream misf (pass_size_s);
				misf >> pass_size;
				
				if(pass_size_s.empty()){
					goto pass_size_emp;
				}
			}
			
		pass_size_rest:
			if(priv){
				while(pass_size <= 0 || pass_size > 10){
					gotoXY(15,13); cout << "\t             ";
					gotoXY(15,13); getline(cin, pass_size_s);
						
					stringstream misf (pass_size_s);
					misf >> pass_size;
									
					if(pass_size_s.empty()){
						goto pass_size_emp;
					}
					if(string::npos != pass_size_s.find_first_of("qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM{}|[];'<>,./?@#$%&*()`~^\\\"")){
						goto pass_size_let;
					}
				}
			}
			else{
				while(pass_size <= 0 || pass_size > 6){
					gotoXY(15,13); cout << "\t             ";
					gotoXY(15,13); getline(cin, pass_size_s);
					
					stringstream misf (pass_size_s);
					misf >> pass_size;
					
					if(pass_size_s.empty()){
						goto pass_size_emp;
					}
					if(string::npos != pass_size_s.find_first_of("qwertyuiopasdfghjklzxcvbnmQWERTYUIOPASDFGHJKLZXCVBNM{}|[];'<>,./?@#$%&*()`~^\\\"")){
						goto pass_size_let;
					}
				}
			}
			
		system("cls");
	
	box_6:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,20); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
		
		gotoXY(10,3); cout << "MERC AIRLINE";
		
	ShowConsoleCursor(false);
	
	Pass_Data_Storing:
		int pass_count = 0, pass_age_check[3], pass_lug[10], pass_age[10], Pass_count = 1, excess_baggage = 0, Darl = 0;
		
		bool insurance[10] = {false,false,false,false,false,false,false,false,false,false};	

		string pass_name[10], pass_age_s, pass_lug_s;
		
	Pass_input:
		
		gotoXY(9,22); cout << "Passenger No. " << Pass_count;
		
		gotoXY(7,6); cout <<  "Please fill in all";
		gotoXY(6,7); cout << "Passenger information";
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,9); cout << b_box;
			b_d_x++;
		}
		
		SetColor(12);
		gotoXY(4,11); cout << "Name:";
		SetColor(10);
		gotoXY(4,13); cout << "Age:";
		gotoXY(4,15); cout << "Luggage Weight:";
		
		while(pass_count < pass_size){
			
			ShowConsoleCursor(true);
			
			//NAME
			gotoXY(9,11); getline(cin,pass_name[pass_count]);
			
			pass_name_emp:
				while(pass_name[pass_count].empty()){
					gotoXY(9,11); getline(cin,pass_name[pass_count]);
				}
				
			pass_name_num:
				while(string::npos != pass_name[pass_count].find_first_of("123456789!@#$%&*()~`[]{};\"\\.><_+-=/?^")){
					gotoXY(9,11); cout << "\t        ";
					gotoXY(9,11); getline(cin,pass_name[pass_count]);
					
					if(pass_name[pass_count].empty()){
						goto pass_name_emp;
					}
				}
			
			SetColor(12);
			gotoXY(4,13); cout << "Age:";
			SetColor(10);
			gotoXY(4,11); cout << "Name:";
			
			//AGE
			gotoXY(8,13); getline(cin,pass_age_s);
			
			pass_age_emp:
				while(pass_age_s.empty()){
					gotoXY(8,13); getline(cin,pass_age_s);
				}
				
			pass_age_let:
				while(string::npos != pass_age_s.find_first_of("QWERTYUIOPASDFGHJKLXCVBNMZabcdefghijklmnopqrstuvwxyz!@#$%&*()_-=+*/.></?'\":;\\")){
					gotoXY(8,13); cout << "\t\t    ";
					gotoXY(8,13); getline(cin,pass_age_s);
					if(pass_age_s.empty()){
						goto pass_age_emp;
					}
				}
			
			stringstream msd2 (pass_age_s);
			msd2 >> pass_age[pass_count];
			
			SetColor(12);
			gotoXY(4,15); cout << "Luggage Weight:";
			SetColor(10);
			gotoXY(4,13); cout << "Age:";
			
			gotoXY(19,15); getline(cin,pass_lug_s);
			
			pass_lug_empty:
				while(pass_lug_s.empty()){
					gotoXY(19,15); getline(cin,pass_lug_s);
				}
			
			pass_lug_let:
				while(string::npos != pass_lug_s.find_first_of("QWERTYUIOPASDFGHJKLXCVBNMZabcdefghijklmnopqrstuvwxyz!@#$%&*()_-=+*/.></?'\":;\\")){
					gotoXY(19,15); cout << "\t     ";
					gotoXY(19,15); getline(cin,pass_lug_s);
				}
				
			stringstream asfe (pass_lug_s);
			asfe >> pass_lug[pass_count];
			
			box_8:
				system("cls");
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,2); cout << b_box;
					b_d_x++;
					//Sleep(50);
				}
				
				b_d_y = 2;
				
				while(b_d_y < 24){
					gotoXY(2,b_d_y); cout << b_box;
					//gotoXY(55,b_d_y); cout << b_box;
					gotoXY(30,b_d_y); cout << b_box;
					b_d_y++;
					//Sleep(50);
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,24); cout << b_box;
					b_d_x++;
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,20); cout << b_box;
					b_d_x++;
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,4); cout << b_box;
					b_d_x++;
				}
				
				gotoXY(10,3); cout << "MERC AIRLINE";
				
			pass_insurance:
				cst_undo_d=true;
				
				ShowConsoleCursor(false);
				
				cst_undo_state = 0;
				
				gotoXY(7,6); cout << "   Do you want  ";
				gotoXY(5,7); cout << "to avail an Insurance?";
				gotoXY(12,9); cout << "[YES]";
				gotoXY(12,11); cout << "[NO]";
				
				while(cst_undo_d){
				
					system("pause>nul");
					
					if(GetAsyncKeyState(VK_UP)){
						cst_undo_state--;
						goto cst_undo_sub3;
					}
					if(GetAsyncKeyState(VK_DOWN)){
						cst_undo_state++;
						goto cst_undo_sub3;
					}
					if(GetAsyncKeyState(VK_LEFT)){
						goto cst_undo_sub3;
					}
					if(GetAsyncKeyState(VK_RIGHT)){
						goto cst_undo_sub3;
					}
					if(GetAsyncKeyState(VK_RETURN)){
						switch(cst_undo_state){
							case 1:
								insurance[pass_count] = true;
								Darl++;
								cst_undo_d = false;
								break;
							case 2:
								cst_undo_d = false;
								break;
						}
					}
					
					cst_undo_sub3:
						switch(cst_undo_state){
							case 0:
								cst_undo_state = 2;
								goto cst_undo_sub3;
								break;
								
							case 1:
								SetColor(12);
								gotoXY(10,9); cout << "[  YES  ]";
								SetColor(10);
								gotoXY(10,11); cout << "  [NO]   ";
								break;
								
							case 2:
								SetColor(12);
								gotoXY(10,11); cout << "[  NO   ]";
								SetColor(10);
								gotoXY(10,9); cout << "  [YES]   ";
								break;
							default:
								cst_undo_state = 1;
								goto cst_undo_sub3;
								break;
						}
				}
			
			box_7:
				system("cls");
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,2); cout << b_box;
					b_d_x++;
					//Sleep(50);
				}
				
				b_d_y = 2;
				
				while(b_d_y < 24){
					gotoXY(2,b_d_y); cout << b_box;
					//gotoXY(55,b_d_y); cout << b_box;
					gotoXY(30,b_d_y); cout << b_box;
					b_d_y++;
					//Sleep(50);
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,24); cout << b_box;
					b_d_x++;
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,20); cout << b_box;
					b_d_x++;
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,4); cout << b_box;
					b_d_x++;
				}
				
				gotoXY(10,3); cout << "MERC AIRLINE";
			
			pass_yn:
				cst_undo_d=true;
				
				cst_undo_state = 0;
				
				gotoXY(5,6); cout << "Is all of that correct?";
				gotoXY(12,9); cout << "[YES]";
				gotoXY(12,11); cout << "[NO]";
				
				while(cst_undo_d){
				
					system("pause>nul");
					
					if(GetAsyncKeyState(VK_UP)){
						cst_undo_state--;
						goto cst_undo_sub2;
					}
					if(GetAsyncKeyState(VK_DOWN)){
						cst_undo_state++;
						goto cst_undo_sub2;
					}
					if(GetAsyncKeyState(VK_LEFT)){
						goto cst_undo_sub2;
					}
					if(GetAsyncKeyState(VK_RIGHT)){
						goto cst_undo_sub2;
					}
					if(GetAsyncKeyState(VK_RETURN)){
						switch(cst_undo_state){
							case 1:
								cst_undo_d = false;
								pass_count++;
								Pass_count++;
								break;
							case 2:
								cst_undo_d = false;
								goto box_10;
								break;
						}
					}
					
					cst_undo_sub2:
						switch(cst_undo_state){
							case 0:
								cst_undo_state = 2;
								goto cst_undo_sub2;
								break;
								
							case 1:
								SetColor(12);
								gotoXY(10,9); cout << "[  YES  ]";
								SetColor(10);
								gotoXY(10,11); cout << "  [NO]   ";
								break;
								
							case 2:
								SetColor(12);
								gotoXY(10,11); cout << "[  NO   ]";
								SetColor(10);
								gotoXY(10,9); cout << "  [YES]   ";
								break;
							default:
								cst_undo_state = 1;
								goto cst_undo_sub2;
								break;
						}
				}
			
			box_10:
				system("cls");
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,2); cout << b_box;
					b_d_x++;
					//Sleep(50);
				}
				
				b_d_y = 2;
				
				while(b_d_y < 24){
					gotoXY(2,b_d_y); cout << b_box;
					//gotoXY(55,b_d_y); cout << b_box;
					gotoXY(30,b_d_y); cout << b_box;
					b_d_y++;
					//Sleep(50);
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,24); cout << b_box;
					b_d_x++;
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,20); cout << b_box;
					b_d_x++;
				}
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,4); cout << b_box;
					b_d_x++;
				}
				
				gotoXY(10,3); cout << "MERC AIRLINE";
				
				gotoXY(7,6); cout <<  "Please fill in all";
				gotoXY(6,7); cout << "Passenger information";
				
				b_d_x = 2;
				
				while(b_d_x <= 30){
					gotoXY(b_d_x,9); cout << b_box;
					b_d_x++;
				}
				
				SetColor(12);
				gotoXY(4,11); cout << "Name:";
				SetColor(10);
				gotoXY(4,13); cout << "Age:";
				gotoXY(4,15); cout << "Luggage Weight:";
				
				
				gotoXY(9,22); cout << "Passenger No. " << Pass_count;
			}
		
	
		system("cls");
	
	Computation:
		float total_price_pass[10], total_price, Vat = 0, total = 0, raw_price = 0, youth = 0, old = 0;
		
		pass_count = 0;
		
		while(pass_count < pass_size){
			
			if(insurance[pass_count]){
				if(priv){
					total_price_pass[pass_count] += 4500;
				}
				else{
					total_price_pass[pass_count] += 8500;
				}
			}
			
			if(priv && pass_lug[pass_count] > 8){
				total_price_pass[pass_count] += (1250*(pass_lug[pass_count]-8));
				excess_baggage += (1250*(pass_lug[pass_count]-8));
			}
			if(buss && pass_lug[pass_count] > 10){
					total_price_pass[pass_count] += (1450*(pass_lug[pass_count]-10));
					excess_baggage += (1450*(pass_lug[pass_count]-10));
			}
			
			if(pass_age[pass_count] <= 13){
				total_price_pass[pass_count] +=  (total_price_pass[pass_count] * .02);
				youth++;
			}
			
			if(pass_age[pass_count] >= 60){
				total_price_pass[pass_count] -= (total_price_pass[pass_count]*.20);
				old++;
			}
			else{
				Vat += total_price_pass[pass_count] * .12;
			}
			
			total += total_price_pass[pass_count];
		
			raw_price +=total_price_pass[pass_count] - (total_price_pass[pass_count]*.12);
			
			pass_count++;
		}
		
	if(round_trip){
		raw_price *= 2;
		total *= 2;
		Vat *= 2;
	}
	
	if(pass_size >= 5){
		total *= 1.05;
	}

	box_20:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
				
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
				
		gotoXY(10,3); cout << "MERC AIRLINE";
	
	Last_booker:
		gotoXY(4,6); cout << "Booker's name:";
		gotoXY(5,7); cout << cst_name;
		
		gotoXY(4,9); cout << "Destination:"; 
		gotoXY(5,10); cout << string_dest[d_sel_state];
		
		gotoXY(4,12); cout << "Class Type:";
		gotoXY(5,13);
		if(priv){
			cout << "Private";	
		}
		else{
			cout << "Business";
		}
		if(round_trip){
			gotoXY(4,15); cout << "Round trip";
		}
		
		gotoXY(4,19); cout << "*************************";
		gotoXY(10,21); cout << "Press Enter";
		gotoXY(10,22); cout << "to continue";
	
		system("pause>nul");
		Sleep(3000);
	
	box_12:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
				
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
				
		gotoXY(10,3); cout << "MERC AIRLINE";
	
	Last_Stretch_pass:
		int lt_pass_counter = 1, lt_pass_y = 8;
		
		gotoXY(10,6); cout << "Passengers";
		pass_count = 0;
		while(pass_count < pass_size){
			gotoXY(4,lt_pass_y); cout << lt_pass_counter << "). " << pass_name[pass_count];
			pass_count++;
			lt_pass_counter++;
			lt_pass_y++;
		}
		gotoXY(4,19); cout << "*************************";
		gotoXY(10,21); cout << "Press Enter";
		gotoXY(10,22); cout << "to continue";
		
		
		system("pause>nul");
		Sleep(3000);
		
	box_13:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
		
		b_d_y = 2;
		
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
			//Sleep(50);
		}
		
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
				
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
				
		gotoXY(10,3); cout << "MERC AIRLINE";	
		
	last_stretch_rock:
		int checker = 0;
		
		gotoXY(4,6); cout << "Travel Fare:" << price_sp;
		
		gotoXY(4,8); cout << "Vatable Amount: P" << raw_price;
		gotoXY(4,9); cout << "Vat: P" << Vat;
		gotoXY(4,10); cout << "Insurance Availed:" << Darl;
		gotoXY(4,11); cout << "Excess Baggage:" << excess_baggage <<" kg.";
		gotoXY(4,12); cout << "Total Discounts:" ;
		if(pass_size > 5){
			gotoXY(4,13); cout << "5% Dis. 5 persons & above";
			
		}
		if(youth > 0){
			gotoXY(4,14); cout << youth << "= 2% Dis. for below 14";
		}
		if(old > 0){
			gotoXY(4,15); cout << old << "= 20% Dis. for Seniors";
		}
		
		gotoXY(4,18); cout << "Total amount: P" << total;
		
		gotoXY(4,20); cout << "*************************";
		gotoXY(10,21); cout << "Press Enter";
		gotoXY(10,22); cout << "to continue";
		
		system("pause>nul");
		Sleep(3000);
		
	box_21:
		system("cls");
		b_d_x = 2;
		
		while(b_d_x <= 30){
			gotoXY(b_d_x,2); cout << b_box;
			b_d_x++;
			//Sleep(50);
		}
				
		b_d_y = 2;
			
		while(b_d_y < 24){
			gotoXY(2,b_d_y); cout << b_box;
			//gotoXY(55,b_d_y); cout << b_box;
			gotoXY(30,b_d_y); cout << b_box;
			b_d_y++;
				//Sleep(50);
		}
			
		b_d_x = 2;
			
		while(b_d_x <= 30){
			gotoXY(b_d_x,24); cout << b_box;
			b_d_x++;
		}
		
		b_d_x = 2;
			
		while(b_d_x <= 30){
			gotoXY(b_d_x,20); cout << b_box;
			b_d_x++;
		}
			
		b_d_x = 2;
				
		while(b_d_x <= 30){
			gotoXY(b_d_x,4); cout << b_box;
			b_d_x++;
		}
				
		gotoXY(10,3); cout << "MERC AIRLINE";
		
	system("cls");
	goto Box_Design;
}
void gotoXY(int x, int y) 
{ 
	CursorPosition.X = x; 
	CursorPosition.Y = y; 
	SetConsoleCursorPosition(console,CursorPosition); 
}
