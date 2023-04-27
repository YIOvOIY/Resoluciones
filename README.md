#include <iostream>
#include <string>
#include <vector>
using namespace std;
class Producto
{
    private:
        string nombre;
        float precio;
        int stock;
        int op1;
        int i=0;
    public:
        Producto(string nombre, float precio, int stock)
        {
            this->nombre = nombre;
            this->precio = precio;
            this->stock = stock;
        }
        void imprimir()
        {
            cout<<"Los datos del producto fueron: "<<endl;
            cout<<"Nombre: "<<nombre<<endl;
            cout<<"Precio: "<<precio<<endl;
            cout<<"Stock: "<<stock<<endl;
        }
        ~Producto()
        {
            cout<<"Ejecutando destructor en: "<<nombre<<endl;
        } 
        string getNombre()
        {
            return nombre;
        }
        void setNombre()
        {
            cout<<"Ingrese nombre: ";cin>>nombre;
        }
        float getPrecio()
        {
            return precio;
        }
        void setPrecio()
        {
            cout<<"Ingrese precio: ";cin>>precio;
        }
        int getStock()
        {
            return stock;
        }
        void setstock()
        {
            cout<<"Ingrese stock: ";cin>>stock;
        }
        void menu()
        {
            while (op1 != 10)
            {
                i=i+1;
                cout<<"_____________________"<<endl;
                cout<<"Bienvenido cliente"<<endl;
                cout<<"Que desea hacer: "<<endl;
                cout<<"1.Crear producto"<<endl;
                cout<<"2.Ver producto"<<endl;
                cout<<"10.Salir"<<endl;
                cout<<"Ingrese opcion: "<<endl;
                cin>>op1;
                switch (op1)
                {
                case 1:
                    setNombre();
                    setPrecio();
                    setstock();
                    break;
                case 2:
                    imprimir();
                    break;
                case 10:
                    cout<<"Gracias por usar este algoritmo"<<endl;
                default:
                    break;
                }
            }
        }

};

int main()
{
    Producto producto0("",1,1);
    producto0.menu();
    return 0;
} 
