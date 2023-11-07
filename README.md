# Tugas_Setter-And-Getter

using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Text; 
using System.Threading.Tasks; 

namespace TugasPert7
{
    public class Pegawai
    {


        private string nama;
        private double gajiPokok;

        public void setNama(string nama)
        {
            this.nama = nama;
        }
        public string getNama() { return this.nama; }

        public double getGajiPokok() { return this.gajiPokok; }

        public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

        public void cetakinfo()
        {

            Console.WriteLine("Nama : " + this.nama);
            Console.WriteLine("Gapok : " + this.gajiPokok);
        }
    }


    public class manager : Pegawai
    {

        private double tunjangan;

        public void setTunjangan(double tunjangan) { this.tunjangan = tunjangan; }
        public double getTunjangan() { return this.tunjangan; }

        public new void cetakinfo()
        {

            base.cetakinfo();
            this.cetakTunjangan();
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + this.tunjangan);

        }
    }

    public class Programmer : Pegawai
    {
        private double bonus;


        public void setBonus(double bonus) { this.bonus = bonus; }

        public double getBonus() { return this.bonus; }

        public new void cetakinfo()
        {
            base.cetakinfo();
            this.cetakBonus();
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus : " + this.bonus);


        }

    }
    class program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("==== PEGAWAI ====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Midun Hakiki");
            pegawai.setGajiPokok(2000000);
            pegawai.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== MANAGER ====");
            manager Manager = new manager();
            Manager.setNama("Midun Hakiki");
            Manager.setGajiPokok(3000000);
            Manager.setTunjangan(1500000);
            Manager.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== PROGRAMMER ====");
            Programmer programer = new Programmer();
            programer.setNama("Midun Hakiki");
            programer.setGajiPokok(4000000);
            programer.setBonus(2500000);
            programer.cetakinfo();
            Console.WriteLine();


            Console.WriteLine("press anykey");
            Console.ReadKey();
        }
    }
}

#  HASILNYA
![Hasil](https://github.com/Midun2103/Tugas_Setter-And-Getter/assets/116275586/cbe71d2e-eef7-4d46-bf62-8150e7b23e8a)
