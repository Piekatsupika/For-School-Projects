#include<stdio.h>
#include<string.h>

int main()
{
    int id,unit;
    float rate, fcgh=0, gamt,amt, ttl;
    char name[35];

    printf("Customer ID:   ");
    scanf("%d", &id);
    printf("Customer name:   ");
    scanf("%s", &name);
    printf("Unit Consumed:   ");
    scanf("%d", &unit);

    if(unit>199 && unit<250)
        rate=1.50;
    else if(unit>250 && unit<400)
        rate=1.60;
    else if(unit>450 && unit<600)
        rate=1.85;
    else
        rate=2;

    gamt=unit*rate;
    if(gamt>400)
        fcgh=gamt*12/100;
    amt=gamt+fcgh;
    if (amt<50)
        amt=50;
    ttl=gamt+fcgh+amt;
    printf("\nElectricity Bill\n");
    printf("Costumer ID                     :%d\n", id);
    printf("Costumer name                   :%s\n", name);
    printf("Unit Consumed                   :%d\n", unit);
    printf("Amount Charges @P %4.2f per unit:%8.2f\n", rate, gamt);
    printf("Surcharge Amount                :%8.2f\n", fcgh);
    printf("Net Amount                      :%8.2f\n", amt);
    printf("\nTotal Bill                    :%8.2f", ttl);

return 0;
}

