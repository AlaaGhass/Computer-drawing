#include <iostream>
#include <graphics.h>
#include <conio.h>


using namespace std;


void drawShape() {
  cleardevice(); 
    circle(100, 50, 40); 
    getch();
}

///////////////////////////////////////////////////

void drawRectangle() {
	
    cleardevice(); 

   
    setbkcolor(YELLOW);
    
    cleardevice();


    settextstyle(SIMPLEX_FONT, HORIZ_DIR, 2);
    setcolor(BLUE);
    
    outtextxy(50, 20, (char *)"rectangle");

    
    setcolor(RED);
    setfillstyle(SOLID_FILL, GREEN);


    rectangle(100, 100, 200, 200);
    
    
    floodfill(150, 150, RED);

    getch();
}

///////////////////////////////////////////////////

//3
void reflectX() {
	
    cleardevice(); 

    line(100, 100, 200, 200);         
    line(100, 300 - 100, 200, 300 - 200);

    getch(); 
}

///////////////////////////////////////////////////

void clipping() {
	
    cleardevice(); 

    int xmin = 100, ymin = 100, xmax = 300, ymax = 300;
        setcolor(RED);
    int lines[4][4] = {
        {50, 150, 250, 150},
        {150, 50, 150, 350},
        {50, 50, 350, 350},
        {100, 200, 300, 300}};
        
      //rectangle(100,100,300,300); 
    rectangle(xmin, ymin, xmax, ymax); 

    for (int i = 0; i < 4; i++) {
        line(lines[i][0], lines[i][1], lines[i][2], lines[i][3]);
    }

    getch();
}

///////////////////////////////////////////////////

void mainMenu() {

 initwindow(600, 600, "Graphics Window");
 
    while (true) {
        cout << "\nMAIN MENU:\n";
        cout << "1. Draw Shape\n";
        cout << "2. Draw Rectangle\n";
        cout << "3. Apply Transformations\n";
        cout << "4. Clipping Example\n";
        cout << "5. Exit\n";
        cout << "Enter your choice: ";

        int choice;
        cin >> choice;

        switch (choice) {
            case 1:
                drawShape();
                break;
            case 2:
                drawRectangle();
                break;
            case 3:
                reflectX();
                break;
            case 4:
                clipping();
                break;
            case 5:
                cout << "Exiting program. Goodbye!\n";
                closegraph(); 
                return;
            default:
                cout << "Invalid choice! Try again.\n";
        }
    }
}

int main() {
    mainMenu();
    return 0;
}
