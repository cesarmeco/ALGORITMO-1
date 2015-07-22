# ALGORITMO-1

//UN MENU QUE TRABAJA CON ARRAYS DE ARRAYS

#include <iostream>
#include <conio.h>
using namespace std;

#define fil 20
#define col 20

void cargar(int vec[col][fil],int m, int n);

void mostrar (int vec[col][fil],int m, int n);

int sumartodo(int vec[col][fil],int m, int n);

void sumarfilas(int vec[col][fil],int m, int n);


void sumarfilas2(int vec[col][fil],int m, int n,int v[]);

int sumarts(int vec[col][fil],int m, int n);

void main()
{int a,b,vec[col][fil],x,m,v[20];
cout<<endl<<"ingresar el tamaño de las columnas"<<endl;
cin>>b;
cout<<"ingresar el tamaño de las filas"<<endl;
cin>>a;

system("cls");
do
	{
	cout<<"*********MENU*********"<<endl<<endl;
	cout<<"1.- cargar"<<endl;
	cout<<"2.- mostrar"<<endl;
	cout<<"3.- sumar todo"<<endl;
	cout<<"4.- sumar triangulo superior"<<endl;
	cout<<"5.- sumar por fila 2.0"<<endl;
	cout<<"6.- sumar por fila"<<endl;
	cout<<"opcion: ";
	cin>>x;
	switch(x)
		{case 1:
		cargar(vec,a, b);
		break;

		case 2:
		mostrar(vec,a, b);
		break;

		case 3:
		m=sumartodo(vec,a, b);
		cout<<m<<endl;
		break;
		case 4:
		m=sumarts (vec,a, b);
		cout<<m<<endl;
		break;

		case 5:
		sumarfilas2(vec,a, b,v);
		for(int i=0;i<a;i++)
		cout<<v[i]<<endl;
		break;

		case 6:
		sumarfilas(vec,a, b);

		cout<<endl;
		break;

		getch();
		system("cls");
		}


	}while(x!=7);

}

void cargar(int vec[col][fil],int m, int n)
{for(int i=0;i<m;i++)
	{for(int k=0;k<n;k++)
		{cout<<"vec["<<k+1<<"]["<<i+1<<"]"<<endl;
		cin>>vec[k][i];
		}
	}
}

void mostrar (int vec[col][fil],int m, int n)
{for(int i=0;i<m;i++)
	{for(int k=0;k<n;k++)
		{cout<<vec[k][i];
		}
	cout<< endl;
	}
}

int sumartodo(int vec[col][fil],int m, int n)
{int s=0;
{for(int i=0;i<m;i++)
	{for(int k=0;k<n;k++)
		{s=s+vec[k][i];
		}
	
	}
}
return s;
}

void sumarfilas(int vec[col][fil],int m, int n)
{int s=0;
{for(int i=0;i<m;i++)
	{for(int k=0;k<n;k++)
		{s=s+vec[k][i];
		
		}
cout<<s<<endl;
s=0;
	
	}
}

}
void sumarfilas2(int vec[col][fil],int m, int n,int v[])
{int s=0;
{for(int i=0;i<m;i++)
	{for(int k=0;k<n;k++)
		{s=s+vec[k][i];
		
		}
v[i]=s;
s=0;
	
	}
}

}

int sumarts(int vec[col][fil],int m, int n)
{int s=0;
for(int i=0;i<m;i++)
	{for(int k=0;k<n;k++)
		{if(k>i)
		s=vec[k][i]+s;	
		}
	}
return s;
}













// CUENTA EL NUMERO DE CARACTERES PEDIDO
#include "stdio.h"
#include "conio.h"
#include <iostream>
#include <string>

using namespace std;
int repetidos(string vec);



void main()
{string vec;
int cont;
cout<<"Ingrese palabra: ";
getline(cin,vec);
cont=repetidos(vec);
cout<<endl<<"El caracter esta repetido "<<cont<<" veces";
getch();
}

int repetidos(string vec)
{	int i,n,c=0;
	char x;
	n = vec.length();
	cout<<"Ingrese un caracter: "<<endl;
	cin>> x;
	for (i=0; i<n; i++)
		{if (vec[i]==x)
			{
			c++;
			}
		}
return (c);
}











//CARGA PLANILLA DE ESTUDIANTES

#include "stdio.h"
#include <conio.h>
#include <iostream>
#include <string>

using namespace std;

struct registro0
{string nombre;
string apellido;
int codigo;
int edad;
};

void main()
{int n;

registro0 registro[10];
cout<<"Ingresar el numero de alumnos: ";
cin>>n;

for(int i=0;i<n;i++)
	{cout<<"Ingresar el nombre del estudiante: ";
	cin.ignore();
	getline(cin,registro[i].nombre);
	cout<<"Ingresar el apellido del estudiante: ";
	cin.ignore();
	getline(cin,registro[i].apellido);
	cout<<"Ingresar edad: ";
	cin>>registro[i].edad;
	cout<<"Ingresar el codigo: "<<endl;
	cin>>registro[i].codigo;

	
	}
system("cls");
cout<<"APELLIDO\tNOMBRE\tEDAD\tCODIGO\t"<<endl;
for(int i=0;i<n;i++)
	{
		cout<<registro[i].apellido<<"\t\t"<<registro[i].nombre<<"\t"<<registro[i].edad<<"\t"<<registro[i].codigo<<"\n";

	}

getch();


}



