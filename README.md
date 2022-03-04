#include <stdio.h>
#include<stdlib.h>
int main()
{
   system("Color 4F");
   int year,month,day,daysinmonth,weekday,firstday;
   printf("\nEnter the desired year:");
   scanf("%d",&year);

   char *months[]={"January","February","March","April","May","June","July","August","September","October","November","December"};
   int monthday[]={31,28,31,30,31,30,31,31,30,31,30,31};

   if((year%4==0&&year%100!=0)||year%400==0)
       monthday[1]=29;

daysinmonth=monthday[month]+1;
   for(month=0;month<12;month++)
    {
      printf("\n\n---------------%s-------------------\n",months[month]);
      printf("\n  Sun  Mon  Tue  Wed  Thurs  Fri  Sat\n");

      for(weekday=0;weekday<firstday;weekday++)
        printf("     ");

      for(day=1;day<=daysinmonth;day++)
        {
        printf("%5d",day);

        if(++weekday>6){
            printf("\n");
            weekday=0;
        }
        }
     }
int startingday(int year)
{

  int d;
  d = (((year - 1) * 365) + ((year - 1) / 4) - ((year - 1) / 100) + ((year) / 400) + 1) % 7;
  return d;
}
}
