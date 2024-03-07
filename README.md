# gt#include <stdio.h>//ham printf
#include <graphics.h>
#include <conio.h>//ham getch(), kbhit()
#include <stdlib.h>//ham random, exit
#include <dos.h>//ham delay

const CHAM = 10;
int mx, my;
void khoitao();
void vecot();

void main()
{
	int dx = 10;
	khoitao();
	vecot();
	while (!kbhit())
	{
		setcolor(random(16));
		circle(mx, my, dx);
		delay(CHAM);
		dx = dx + 10;
		if (dx > 2 *my)
		{
			delay(20 *CHAM);
			dx = 10;
			vecot();
		}
	}#include <stdio.h>//ham printf
#include <graphics.h>
#include <conio.h>//ham getch(), kbhit()
#include <stdlib.h>//ham random, exit
#include <dos.h>//ham delay

const CHAM = 10;
int mx, my;
void khoitao();
void vecot();

void main()
{
	int dx = 10;
	khoitao();
	vecot();
	while (!kbhit())
	{
		setcolor(random(16));
		circle(mx, my, dx);
		delay(CHAM);
		dx = dx + 10;
		if (dx > 2 *my)
		{
			delay(20 *CHAM);
			dx = 10;
			vecot();
		}
	}

	closegraph();
}

void vecot()
{
	setbkcolor(BLUE);
	cleardevice();
	setcolor(RED);
	setfillstyle(6, LIGHTRED);
	line(mx, my, mx - 20, my + 15);
	line(mx, my, mx + 20, my + 15);
	line(mx - 20, my + 15, mx - 40, 2 *my);
	line(mx + 20, my + 15, mx + 40, 2 *my);
	line(mx - 40, 2 *my, mx + 40, 2 *my);
	floodfill(mx, my + 20, RED);
}

void khoitao()
{
	int gdrv = DETECT, gmode, errorcode;
	initgraph(&gdrv, &gmode, "..\\BGI");
	errorcode = graphresult();
	if (errorcode != grOk)
	{
		printf("Graphics error : %s\n", grapherrormsg(errorcode));
		printf("Press any key to halt ...");
		getch();
		exit(1);
	}

	mx = getmaxx() / 2;
	my = getmaxy() / 2;
}));
		printf("Press any key to halt ...");
		getch();
		exit(1);
	}

	mx = getmaxx() / 2;
	my = getmaxy() / 2;
}
