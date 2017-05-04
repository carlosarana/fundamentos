# fundamentos
package fundamento; 
  //Variables o metodos de clases son static
  //Variables o metodos de instancia no son static.
  //Para acceder a un metodo o variable static es : NombreClass.Metodo
  // o NombreClase.Variable

   class CuentaBancaria{
      public int saldo;
       public static int numero=0;
    }
      
    public class variables {
      
        public static void sumarSaldo(CuentaBancaria cta){
             cta.saldo +=20;
        }
         
        public static void sumarSaldo(int saldo){
            saldo +=20;
        }   
        
        //Crear  10 objeto de CuentaBancaria, probar y probar. 
    public static void main(String[] args) {
        
        CuentaBancaria ct1= new CuentaBancaria();
        CuentaBancaria ct2=ct1;
        ct1.saldo=1000;
        
        
        sumarSaldo(ct1);
        sumarSaldo(ct2);
        System.out.println("ct1:" +ct1.saldo);//imprime 1040
        System.out.println("ct2:"+ct2.saldo);//imprime 1040
        
        ct2.saldo=270;
        CuentaBancaria ct3 = ct2;
        sumarSaldo(ct3);
        System.out.println("ct3:" +ct3.saldo);//imprime 290
        
        ct3.saldo=1400;
        CuentaBancaria ct4 = ct3;
        sumarSaldo (ct4);
        System.out.println("ct4:" +ct4.saldo); //imprime 1420
        
        CuentaBancaria ct5 = ct4;
        sumarSaldo (ct5);
        System.out.println("ct5:" +ct5.saldo);//imprime 1440
        
        CuentaBancaria ct6 = new CuentaBancaria();
        ct6.saldo=160;
        CuentaBancaria ct7 = ct2;
        ct7.saldo=1400;
        sumarSaldo (ct6);
        sumarSaldo (ct7);
        System.out.println("ct6:" +ct6.saldo);//imprime 180
        System.out.println("ct7:"+ct7.saldo);//imprime 1420
        
        CuentaBancaria ct8 = ct3;
        sumarSaldo (ct8);
        CuentaBancaria ct9 = ct6;
        sumarSaldo (ct9);
        CuentaBancaria ct10 = new CuentaBancaria();
        ct10.saldo=1200;
        sumarSaldo (ct10);
        System.out.println("ct8:" +ct8.saldo); //imprime 1440
        System.out.println("ct9:" +ct9.saldo); // imprime  200
        System.out.println("ct10:" +ct10.saldo); //imprime 1220
 
    }
    
}
