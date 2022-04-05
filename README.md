# trianguloRetangulo
Calcula a área de um triangulo retângulo


import java.util.Scanner;

public class uni {
    public static void main(String[]args){//entry da aplicação
        try (Scanner leitor = new Scanner(System.in)) {
            System.out.println("digite a coord. X do ponto p1");
            int p1X = leitor.nextInt();
            System.out.println("digite a coord. Y do ponto p1");
            int p1Y = leitor.nextInt();
            System.out.println("digite a coord. X do ponto p2");
            int p2X = leitor.nextInt();
            System.out.println("digite a coord. Y do ponto p2");
            int p2Y = leitor.nextInt();
            System.out.println("digite a coord. X do ponto p3");
            int p3X = leitor.nextInt();
            System.out.println("digite a coord. Y do ponto p3");
            int p3Y = leitor.nextInt();
            //pontos digitados pelo usuario dentro da TAD "TrianguloRetangulo"
            TrianguloRetangulo tr = new TrianguloRetangulo();
            tr.p1X = p1X;
            tr.p1Y = p1Y;
            tr.p2X = p2X;
            tr.p2Y = p2Y;
            tr.p3X = p3X;
            tr.p3Y = p3Y;
            
            double area = tr.calculaArea();
            double perimetro = tr.calculaPerimetro ();

            System.out.println("Para os pontos do triangulo retangulo digitado, segue abaixo o relatorio");
            System.out.println("Area"+area);
            System.out.println("Perimetro"+perimetro);

        }
    }  
}


//faça um arquivo java para guardar os valores de p1, p2 e p3.
public class TrianguloRetangulo {
   //atributos(dados da TAD)
   int p1X,p1Y;
   int p2X,p2Y;
   int p3X,p3Y;
   //metodo
   public double calculaArea(){
       int c1 = Math.abs(p1Y - p2Y);//cateto c1
       int c2 = Math.abs(p3X - p2X);//cateto c1
       double area = (c1*c2)/2;//area
       return area;
   }
   public double calculaPerimetro(){
       int c1 = Math.abs(p1Y - p2Y);
       int c2 = Math.abs(p3Y - p2Y);
       double h = Math.sqrt(Math.pow(c1,2) + Math.pow(c2,2));
       double perimetro = c1+c2+h;
    return perimetro;
   }
}


