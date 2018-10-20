package banco;

// Classe contaBanco
public class ContaBanco {
	String nome;
	String numero_Conta;
	double valorSaldo = 0, balance = 100;
	
	// Receber nome do cliente
	public String nomeCliente() {
		return nome;
	}
	
	// Receber numero da conta
	public String contaCliente() {
		return numero_Conta;
	}
	
	// Mostrar saldo atual
	public double balance() {
		System.out.println("saldo atual: "+balance);
		return balance;
	}
	
	// Sacar
	double sacar(double valor_saque) {
		balance -= (valor_saque);
		return (balance);
	}
	
	// Depositar
	double depositar(double valor_deposito) {
		balance += (valor_deposito);
		return (balance);
	}
	
	// Mostrar saldo atual (Manter essa e deletar a primeira ln.19 ou deletar essa)
	double checkBalance() {
		return balance;
	}
	
	// Alterar nome do cliente
	public String alterarNome(String newName){
		nome = newName;
		return nome;
	}
	
	// Mostrar nome do cliente
	public String consultarNome() {
		return nome;
	}
	

}

