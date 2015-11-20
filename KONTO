#include <iostream>
#include <cstring>
#include <stdlib.h>
using namespace std;

enum oprocentowanie {classic,pluss,premium} ;

class Konto {
public:
    string nazwisko;
    double saldo;
    int pin;
    oprocentowanie procent;

    void stworzKonto(string nazw,double saldo_pocz,int nr_pin,oprocentowanie procent);

    void podajOprocentowanie();

    bool sprawdzPin(int nr_pin);

    double dokonajWplaty(double wplata);

    int dokonajWyplaty(double wyplata,int nr_pin);

    int zmienPin(int nr_pin);

};
//*************************************************************

void Konto::stworzKonto(string nazw,double saldo_pocz,int nr_pin,oprocentowanie procent)
{
 nazwisko=nazw;
 saldo=saldo_pocz;
 pin=nr_pin;
 procent=procent;
}

void Konto::podajOprocentowanie()
{
    switch (procent)
    {
        case classic:
        cout<<"Oprocentowanie wynosi 0%"<<endl;
        break;
        case pluss:
        cout<<"Oprocentowanie wynosi 3%"<<endl;
        break;
        case premium:
        cout<<"Oprocentowanie wynosi 5%"<<endl;
        break;

    }
}


bool Konto::sprawdzPin(int nr_pin)
{
    if (pin==nr_pin)
    return true;
    else
    return false;
}
double Konto::dokonajWplaty(double wplata)
{

    if (wplata>0)
        saldo=saldo+wplata;
    return saldo;
}
int Konto::dokonajWyplaty(double wyplata, int nr_pin)
{
    if ((pin==nr_pin)&&(wyplata<=saldo))
        {
            saldo=saldo-wyplata;
            return 0;
        }
else return 1;
}
int Konto::zmienPin(int nr_pin)
{
    if (pin==nr_pin)
        {
            pin=nr_pin;
            return 0;
        }
    else return 1;
}


int main()
{
 int nr_pin;
 double wplata;
 Konto MojeKonto;
 MojeKonto.nazwisko="Szymanski";
 MojeKonto.saldo=10000;
 MojeKonto.pin=1234;
 MojeKonto.procent=pluss;
 system("cls");
 MojeKonto.podajOprocentowanie();
 cout<<"Podaj pin"<<endl;
 cin>>nr_pin;
 if (MojeKonto.sprawdzPin(nr_pin)==true)
     cout<<"PIN zgodny"<<endl;
 else
     cout<<"Nieprawidlowy PIN"<<endl;
 cout<<"Podaj kwote wplaty"<<endl;
 cin>>wplata;
 cout<<MojeKonto.dokonajWplaty(wplata)<<endl;





    return 0;
}
