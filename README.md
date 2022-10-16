# PBO_Latihan2



//Mengimpor Metode Input Data
import java.util.Scanner;

//Membuat Class AkunBank
public class AkunBank{

    //Membuat Atributt Saldo (Tipe Data Integer)
    Integer saldo = 100000;

    //Instance Method cekSaldo
    void cekSaldo(){
        System.out.println("Saldo Anda Saat Ini: Rp. " + saldo);
    }

    //Instance Method simpanUang
    void simpanUang(){
        Scanner input = new Scanner(System.in);
        System.out.print("Simpan Uang Anda: Rp. ");
        saldo += input.nextInt();
        System.out.println("Saldo Anda Saat Ini: Rp. " +saldo);
    }

    //Instance Method ambilUang
    void ambilUang() {
        Scanner input = new Scanner(System.in);
        System.out.print("Ambil Uang Anda: Rp. ");
        saldo -= input.nextInt();
        System.out.println("Saldo Anda Saat Ini: Rp. " + saldo);
    }
}

//Membuat Class Transaksi Untuk Menampilkan Data di Layar
class Transaksi{
    public static void main(String[] args){
        AkunBank bank = new AkunBank();
        System.out.println("Selamat Datang di Bank INI");
        bank.cekSaldo();
        System.out.println(" ");
        bank.simpanUang();
        System.out.println(" ");
        bank.ambilUang();
    }
}
