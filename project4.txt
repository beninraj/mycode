#include <stdio.h>
void main(){
    int year,month,date,y,m,m_1,m_2,m_3,m_4,t,x,current_year,this_year,day;
    
    printf("enter a year:",year);
    scanf("%d",&year);
    if(year!=0 && year >=2000)
    year=year;
    else
    printf("enter the correct year");
    
    
    printf("enter a month:",month);
    scanf("%d",&month);
    if(month!=0 && month>0 && month <13)
    month=month;
    else
    printf("Please enter the correct month");
     
     
     printf("enter a date:",date);
    scanf("%d",&date);
    if(date!=0 && date>0 && date <32)
    date=date;
    else
    printf("Please enter the correct date");
    
     switch(month)
    {
        case 2: if(year%4==0)
            if(date!=0 && date<30)
            date=date;
            else
            printf("PLease enter the correct date");
        
            else if(year %4!=0)
            if(date!=0 && date<29)
            date=date;
            else
            printf("Please enter the correct date");
        
        case 1:
        case 3:
        case 5:
        case 7:
        case 8:
        case 10:
        case 12:if(date!=0&&date<32)
               date=date;
               else
               printf("Please enter the correct date");
               break;
        case 4:
        case 6:
        case 9:
        case 11:if(date!=0&&date<31)
                date=date;
                else
                printf("Please enter the correct date");
                break;
    }
    if (year>2000){
    y=year%100;
    m=y-1;
    m_1=m/4;
    m_2=m-m_1;
    m_3=m_1*2+m_2*1;
    m_4=m_3 % 7;
    }
    x=month-1;
    switch(x)
    {
        case 1:t=31;
                //printf("%d",t);
               break;
        case 2:if(year%4==0){
               t=60;}
               //printf("%d",t);}
               else 
               t=59;
               //printf("%d",t);
               break;
        case 3:if(year%4==0){
               t=91;}
               //printf("%d",t);}
               else 
               t=90;
               //printf("%d",t);
               break;
        case 4:if(year%4==0){
               t=121;}
               //printf("%d",t);}
               else 
               t=120;
               //printf("%d",t);
               break;
        case 5:if(year%4==0){
               t=152;}
               //printf("%d",t);}
               else 
               t=151;
               //printf("%d",t);
               break;
        case 6:if(year%4==0){
               t=182;}
               //printf("%d",t);}
               else 
               t=181;
               //printf("%d",t);
               break;
        case 7:if(year%4==0){
               t=213;}
               //printf("%d",t);}
               else 
               t=212;
               //printf("%d",t);
               break;
        case 8:if(year%4==0){
               t=244;}
               //printf("%d",t);}
               else 
               t=243;
               //printf("%d",t);
               break;
        case 9:if(year%4==0){
               t=274;}
               //printf("%d",t);}
               else 
               t=273; 
               //printf("%d",t);
               break;
        case 10:if(year%4==0){
               t=305;}
               //printf("%d",t);}
               else 
               t=304; 
               //printf("%d",t);
               break;
        case 11:if(year%4==0){
               t=335;}
               //printf("%d",t);}
               else 
               t=334; 
               //printf("%d",t);
               break;
        case 12:if(year%4==0){
               t=366;}
               //printf("%d",t);}
               else 
               t=365;
               //printf("%d",t);
               break;
    }
    current_year=t+date;
    this_year=current_year % 7;
    day=0+m_4+this_year;
    if(day>6)
    day=day%7;
    else;
    switch(day)
    {
        case 0:printf("SUNDAY");
        break;
        case 1:printf("MONDAY");
        break;
        case 2:printf("");
        break;
        case 3:printf("WEDNESDAY");
        break;
        case 4:printf("THURSDAY");
        break;
        case 5:printf("FRIDAY");
        break;
        case 6:printf("SATURDAY");
        break;
    }
    
}



    
