# ORIENTED OBJECT PROGRAMMING
## Praktikum 3


Membuat Class Pegawai Sebagai Superclass 
dan menambahkan atribut nama serta gaji pokok

      public class Pegawai {

          private String nama;
          private Double gajiPokok;


Membuat setter & getter untuk atribut yang di-private

      public void setNama(String nama){
          this.nama = nama;
      }
      public String getNama(){
          return this.nama;
      }
      public void setGajiPokok(Double gajiPokok){
          this.gajiPokok=gajiPokok;
      }
      public Double getGajiPokok(){
          return this.gajiPokok;
      }


Method cetakInfo digunakan untuk menampilkan data nama pegawai dan gaji pokok.

          public void cetakInfo(){
              System.out.println("Nama Pegawai: " + getNama());
              System.out.println("Gaji Pokok : " + getGajiPokok());
          }
      }
      
      

### Subclasss manager 

        public class Manager extends Pegawai {
            private Double tunjangan;

            public void setTunjangan(Double tunjangan){
                this.tunjangan = tunjangan;
            }
            public Double getTunjangan(){
                return this.tunjangan;
            }
            public void cetakInfo(){
                System.out.println("Nama Pegawai: " + getNama());
                System.out.println("Gaji Pokok  : Rp. " + getGajiPokok());
                System.out.println("Tunjangan   : Rp. " + getTunjangan());
            }

            public static void main(String[] args) {
                Manager managerProd = new Manager();

                managerProd.setNama("Anton");
                managerProd.setGajiPokok(5000000.00);
                managerProd.setTunjangan(10000000.00);


                managerProd.cetakInfo();
            }
        }

