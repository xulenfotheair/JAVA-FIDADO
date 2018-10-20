package banco;

import java.util.Scanner;

public class ContaFuncional {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		Scanner s = new Scanner(System.in);
		ContaBanco conta = new ContaBanco();
		double deposito = 0, saque = 0;
		
		
		System.out.println("Informe seu nome: ");
		conta.nome = s.next();
		System.out.println("Informe o numero da sua conta: ");
		conta.numero_Conta = s.next();
		
		System.out.printf("Informe o que deseja fazer:\n"
				+ "1- Para sacar\n"
				+ "2- Para depositar\n"
				+ "3- Para consultar saldo\n"
				+ "4- Para sair\n");
		String decisao = s.next();
		
		
		
			switch(decisao) {
			case "1":
				conta.balance();
				System.out.println("Quanto deseja sacar? ");
			    saque = s.nextDouble();
				System.out.println("Saldo atual: "+conta.sacar(saque));
				break;
			case "2":
				conta.balance();
				System.out.println("Quanto deseja depositar? ");
			    deposito = s.nextDouble();
				System.out.println("Saldo atual: "+conta.depositar(deposito));
				break;
			case "3":
				conta.checkBalance();
				break;
			case "4":
				System.out.println("Você escolheu sair!");
				break;
				
				default:
					System.err.println("ERROR");
		}

	}

}

