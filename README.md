#include <stdio.h>

int main ()
{
	int month=0;
	int year=0;
	int day=0;
	int month1=0;
	int year1=0;
	int day1=0;
	int jan=31, feb=28,feb1=29,mar=31,apr=30,may=31,jun=30,jul=31,aug=31,sep=30,oct=31,nov=30,dec=31;
	printf("Vvedite vashy datu rozhdenia v formate: dd.mm.yyyy\n");
	scanf("%d.", &day);
	scanf("%d.", &month);
	scanf("%d", &year);
	printf("Vvedite tekushuu datu v formate: dd.mm.yyyy\n");
	scanf("%d.", &day1);
	scanf("%d.", &month1);
	scanf("%d", &year1);
	if (year%4==0 || year%100!=0 && year%400==0) printf("God tvoego rozdenia visokosniy\n");//определение високосности года
	else printf("God tvoego rozdenia ne visokosniy\n");
	int sum=0;
	while ((year+1)<year1)//подсчет дней в целых прошедших годах
	{
		if (year%4==0 || year%100!=0 && year%400==0)
		sum+=366;
		else sum+=365;
		year++;
	}
	if (year%4==0 || year%100!=0 && year%400==0)//подсчет дней в первом году
	{
		switch(month){
			case 1: sum+=366-day;
			break;
			case 2: sum+=366-jan-day;
			break;
			case 3: sum+=366-jan-feb1-day;
			break;
			case 4: sum+=366-jan-feb1-mar-day;
			break;
			case 5: sum+=366-jan-feb1-mar-apr-day;
			break;
			case 6: sum+=366-jan-feb1-mar-apr-may-day;
			break;
			case 7: sum+=366-jan-feb1-mar-apr-may-jun-day;
			break;
			case 8: sum+=366-jan-feb1-mar-apr-may-jun-jul-day;
			break;
			case 9: sum+=366-jan-feb1-mar-apr-may-jun-jul-aug-day;
			break;
			case 10: sum+=366-jan-feb1-mar-apr-may-jun-jul-aug-sep-day;
			break;
			case 11: sum+=366-jan-feb1-mar-apr-may-jun-jul-aug-sep-oct-day;
			break;
			case 12: sum+=366-jan-feb1-mar-apr-may-jun-jul-aug-sep-oct-nov-day;
			break;
			
		}
	}
	else {
		switch(month){
			case 1: sum+=365-day;
			break;
			case 2: sum+=365-jan-day;
			break;
			case 3: sum+=365-jan-feb-day;
			break;
			case 4: sum+=365-jan-feb-mar-day;
			break;
			case 5: sum+=365-jan-feb-mar-apr-day;
			break;
			case 6: sum+=365-jan-feb-mar-apr-may-day;
			break;
			case 7: sum+=365-jan-feb-mar-apr-may-jun-day;
			break;
			case 8: sum+=365-jan-feb-mar-apr-may-jun-jul-day;
			break;
			case 9: sum+=365-jan-feb-mar-apr-may-jun-jul-aug-day;
			break;
			case 10: sum+=365-jan-feb-mar-apr-may-jun-jul-aug-sep-day;
			break;
			case 11: sum+=365-jan-feb-mar-apr-may-jun-jul-aug-sep-oct-day;
			break;
			case 12: sum+=365-jan-feb-mar-apr-may-jun-jul-aug-sep-oct-nov-day;
			break;
			
		}
	}
	if (year1%4==0 || year%100!=0 && year%400==0)//подсчет дней в последнем году
	{
		switch(month1){
			case 1: sum+=day1;
			break;
			case 2: sum+=jan+day1;
			break;
			case 3: sum+=jan+feb1+day1;
			break;
			case 4: sum+=jan+feb1+mar+day1;
			break;
			case 5: sum+=jan+feb1+mar+apr+day1;
			break;
			case 6: sum+=jan+feb1+mar+apr+may+day1;
			break;
			case 7: sum+=jan+feb1+mar+apr+may+jun+day1;
			break;
			case 8: sum+=jan+feb1+mar+apr+may+jun+jul+day1;
			break;
			case 9: sum+=jan+feb1+mar+apr+may+jun+jul+aug+day1;
			break;
			case 10: sum+=jan+feb1+mar+apr+may+jun+jul+aug+sep+day1;
			break;
			case 11: sum+=jan+feb1+mar+apr+may+jun+jul+aug+sep+oct+day1;
			break;
			case 12: sum+=jan+feb1+mar+apr+may+jun+jul+aug+sep+oct+nov+day1;
			break;
			
		}
	}
	else
	{
		switch(month1){
			case 1: sum+=day1;
			break;
			case 2: sum+=jan+day1;
			break;
			case 3: sum+=jan+feb+day1;
			break;
			case 4: sum+=jan+feb+mar+day1;
			break;
			case 5: sum+=jan+feb+mar+apr+day1;
			break;
			case 6: sum+=jan+feb+mar+apr+may+day1;
			break;
			case 7: sum+=jan+feb+mar+apr+may+jun+day1;
			break;
			case 8: sum+=jan+feb+mar+apr+may+jun+jul+day1;
			break;
			case 9: sum+=jan+feb+mar+apr+may+jun+jul+aug+day1;
			break;
			case 10: sum+=jan+feb+mar+apr+may+jun+jul+aug+sep+day1;
			break;
			case 11: sum+=jan+feb+mar+apr+may+jun+jul+aug+sep+oct+day1;
			break;
			case 12: sum+=jan+feb+mar+apr+may+jun+jul+aug+sep+oct+nov+day1;
			break;
		}
	}
	printf("%d dney ti uzhe prozhil\n",sum);
	switch(month)// определение знака зодиака по месяцу и дню рождения(используется 12 знаков зодиака)
	{
		case 1: if (day>=1 && day<=19)//january 
		printf("Kozerog");
		else printf("Vodoley");
		break;
		case 2: if(day>=1 && day<=18)//february
		printf("Vodoley");
		else printf("Ribi");
		break;
		case 3: if(day>=1 && day<=20)//march
		printf("Ribi");
		else printf("Oven");
		break;
		case 4: if(day>=1 && day<=19)//april
		printf("Oven");
		else printf("Telets");
		break;
		case 5: if(day>=1 && day<=20)//may
		printf("Telets");
		else printf("Bliznetsi");
		break;
		case 6: if(day>=1 && day<=20)//june
		printf("Bliznetsi");
		else printf("Rak");
		break;
		case 7: if(day>=1 && day<=22)//july
		printf("Rak");
		else printf("Lev");
		break;
		case 8: if(day>=1 && day<=22)//august
		printf("Lev");
		else printf("Deva");
		break;
		case 9: if(day>=1 && day<=22)//september
		printf("Deva");
		else printf("Vesi");
		break;
		case 10: if(day>=1 && day<=22)//october
		printf("Vesi");
		else printf("Skorpion");
		break;
		case 11: if(day>=1 && day<=21)//november
		printf("Skorpion");
		else printf("Strelets");
		break;
		case 12: if(day>=1 && day<=21)//december
		printf("Strelets");
		break;
		default: printf("oshibka v vibore mesyatsa?");
	}
}
