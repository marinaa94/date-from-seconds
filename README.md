# date-from-seconds
#include <stdio.h>
#include <time.h>
   //#define YEAR=1970
int main()
{
long unsigned time_t= time(NULL);
printf("Time in seconds since \"UNIX EPOCH\" Thursday ,1 January 1970 : %lu \n",time_t);
time_t=time_t-(time_t%60);   //time_t=time of seconds
  //printf("%lu ",time_t);
int min= time_t/60;
int time_min=min%60;       //time of minites
int hour=min/60;
int time_hour=hour%24;      //time of hours 
int day=(hour-(hour%24))/24;
int year=day /365;
int date;
 //printf ("%lu,%d,%d,%d,%d,%d,%d \n",time_t,min,time_min,hour,time_hour,day,year);
printf("Printing Leap Years Since 1970 .....\n      ");
const int YEAR=1970;
int i=0;
int n=0;
for (i=0;i<year;i++)
{
 date=YEAR+i;
   //printf("%d ",date);
if (date%4==0)
 {printf("%d ",date);
 n++;}
else if (date%100==0);
   //printf("%d ",date);
else if (date%400==0)
 {printf("%d ",date);
  n++;}
else ;
}
printf("\n      Number of Leap Years Since 1970 is %d \nToday is ",n);
int YY=YEAR+year;       //YY=date of year,YEAR =const 1970,year=varible
 //printf("%d=%d+%d",YY,YEAR,year);
day=day-n+1;
if (YY!=date)
  {int DD= day%365;       //DD=date of day
  // printf("%d=%d ",DD,day);
   if (DD<=31)
    {printf("%d Jan %d",DD,YY);}
  else if(31<DD<=59)
    {DD=DD-31;
    printf("%d Feb %d",DD,YY);}
  else if(59<DD<=90)
    {DD=DD-59;
     printf("%d Mar %d",DD,YY);}
  else if(90<DD<=120)
    {DD=DD-90;
     printf("%d Apr %d",DD,YY);}
  else if(120<DD<=151)
    {DD=DD-120;
     printf("%d May %d",DD,YY);}
  else if(151<DD<=181)
    {DD=DD-151;
     printf("%d Jun %d",DD,YY);}
  else if(181<DD<=212)
    {DD=DD-181;
     printf("%d Jul %d",DD,YY);}
  else if(212<DD<=243)
    {DD=DD-212;
     printf("%d Aus %d",DD,YY);}
  else if(243<DD<=273)
    {DD=DD-243;
     printf("%d Sep %d",DD,YY);}
  else if(273<DD<=304)
    {DD=DD-273;
     printf("%d Oct %d",DD,YY);}
  else if(304<DD<=334)
    {DD=DD-304;
     printf("%d Nov %d",DD,YY);}
  else if(334<DD<=365)
    {DD=DD-334;
     printf("%d Dec %d",DD,YY);}
   else;}
else 
  {int DD=day%365;
  if (DD<=31)
    {printf("%d Jan %d",DD,YY);}
  else if(31<DD<=60)
    {DD=DD-31;
     printf("%d Feb %d",DD,YY);}
  else if(60<DD<=91)
    {DD=DD-60;
     printf("%d Mar %d",DD,YY);}
  else if(91<DD<=121)
    {DD=DD-91;
     printf("%d Apr %d",DD,YY);}
  else if(121<DD<=152)
    {DD=DD-121;
     printf("%d May %d",DD,YY);}
  else if(152<DD<=182)
    {DD=DD-152;
     printf("%d Jun %d",DD,YY);}
  else if(182<DD<=213)
    {DD=DD-182;
     printf("%d Jul %d",DD,YY);}
  else if(213<DD<=244)
    {DD=DD-213;
     printf("%d Aus %d",DD,YY);}
  else if(244<DD<=274)
    {DD=DD-244;
     printf("%d Sep %d",DD,YY);}
  else if(274<DD<=305)
    {DD=DD-274;
     printf("%d Oct %d",DD,YY);}
  else if(305<DD<=335)
    {DD=DD-305;
     printf("%d Nov %d",DD,YY);}
  else if(335<DD<=366)
    {DD=DD-335;
     printf("%d Dec %d",DD,YY);}
  else;};

time_hour=time_hour+2;
printf(" and Time is %d :%d \n",time_hour,time_min);
return 0;
}
