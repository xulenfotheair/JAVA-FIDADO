package banco;

public class ContaBanco {
	String nome;
	String numero_Conta;
	double valorSaldo = 0, balance = 100;
	
	
	public String nomeCliente() {
		return nome;
	}
	
	public String contaCliente() {
		return numero_Conta;
	}
	
	public double balance() {
		System.out.println("saldo atual: "+balance);
		return balance;
	}
	
	double sacar(double valor_saque) {
		balance -= (valor_saque);
		return (balance);
	}
	
	double depositar(double valor_deposito) {
		balance += (valor_deposito);
		return (balance);
	}
	
	double checkBalance() {
		return balance;
	}
	
	
	
	
	public String alterarNome(String newName){
		nome = newName;
		return nome;
	}
	
	public String consultarNome() {
		return nome;
	}
	

}

