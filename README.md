# Ejercicios de DIP, ISP, SRP
## Ejercicio 1 

**DIP:** 
El patron DIP no se cumple. Las clases dependen una de otra, sin que dos clases por ejemplo,dependan de una mas abstracta. 

**ISP:** Este patrón se cumple. Aunque Analizador datos no utilice todas las funciones de base de datos, no hay mas de una clase que utilice diferentes partes de otra clase, por lo que no hay un incumplimiento del patron.

**SRP:** SRP no se cumple. La clase tiene mas de una razon de cambio. Puede cambiar baseDatos.ListarDatos(), como tambien puede cambiar la clase DataBaseObject, y ambos cambios afectarian a AnalizadorDatos.


## Ejercicio 2

```cs
//
class DataBaseObject
{
    public string Descripcion { get; }
}

//Base de datos.
class BaseDeDatos:AbsBaseDatos
{
    public DataBaseObject ObtenerDato(string clave)
    {
        //Devuelve el dato correspondiente a la clave
    }
    public void GrabarDato(string clave, DataBaseObject dato)
    {
        //Graba el dato en la base de datos, bajo la clave dada
    }
    public String[] ListarClaves()
    {
        //Devuelve un String[] con todas las claves
    }
    public String[] ListarDescripcionDatos()
    {
        //Devuelve un String[] con la descripción de todas los 
        //datos almacenados en  la base
    }
    
}
class AnlizadorDatos
{
    private BaseDeDatos baseDatos{get; set;};
    public void Analizar()
    {
        foreach (DataBaseObject DBObj in baseDatos.ListarDatos())
        {
            if (CumpleCondicion(DBObj)==1)
            {
                MensajeUno();
            }
            else if (CumpleCondicion(DBObj)==2)
            {
                MensajeDos();
            }
        }
    }
    
    public int Cumplecondicion(DataBaseObject DBobj)
    {
        //Devuelve un int dependiendo de qué condición se cumple.
    }
    public void MensajeUno()
    { /*Mensaje predeterminado*/ }
    public void MensajeDos()
    { /*Mensaje predeterminado*/ }
    public void MensajeTres(){
        //otro mensaje
    }
}
Public abstract Class AbsBaseDatos{
    public DataBaseObject[] ListarDatos()
    {
//Devuelve un DataBaseObject[] con todos los datos almacenados en la base
    } 

}
private BaseDeDatos baseDatos{get; set;};
    public void Analizar()
    {
        foreach (DataBaseObject DBObj in baseDatos.ListarDatos())
        {
            if (CumpleCondicion(DBObj)==1)
            {
                MensajeUno();
            }
            else if (CumpleCondicion(DBObj)==2)
            {
                MensajeDos();
            }
        }
    }

```
## Ejercicio 3 

```cs
////Insertar el código corregido. El ejercicio 2 y 3 pueden ser resueltos de forma conjunta
public int Cumplecondicion(DataBaseObject DBobj)
    {
        //Devuelve un int dependiendo de qué condición se cumple.
    }
    public void MensajeUno()
    { /*Mensaje predeterminado*/ }
    public void MensajeDos()
    { /*Mensaje predeterminado*/ }
    public void MensajeTres(){
        //otro mensaje
    }

```