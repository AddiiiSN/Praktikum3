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
            public void cetakInfoManager(){
                System.out.println("Nama Pegawai: " + getNama());
                System.out.println("Gaji Pokok  : Rp. " + getGajiPokok());
                System.out.println("Tunjangan   : Rp. " + getTunjangan());
            }

            public static void main(String[] args) {
                Manager managerProd = new Manager();

                managerProd.setNama("Anton");
                managerProd.setGajiPokok(5000000.00);
                managerProd.setTunjangan(10000000.00);


                managerProd.cetakInfoManager();
            }
        }
        
![Screenshot (10)](https://user-images.githubusercontent.com/115928747/199699961-d69911d8-45a6-4213-838d-71fb970f0873.png)



### Subclass Programmer

            public class Programmer extends Pegawai{
                private Double bonus;

                public void setBonus(Double bonus){
                    this.bonus = bonus;
                }

                public Double getBonus() {
                    return bonus;
                }

                public void cetakInfoPogrammer(){
                    System.out.println("Nama Pegawai: " + getNama());
                    System.out.println("Gaji Pokok  : Rp. " + getGajiPokok());
                    System.out.println("Bonus       : Ro. " + getBonus());
                }

                public static void main(String[] args){
                    Programmer programmer1 = new Programmer();

                    programmer1.setNama("Riko");
                    programmer1.setGajiPokok(5000000.00);
                    programmer1.setBonus(5000000.00);

                    programmer1.cetakInfoPogrammer();
                }
            }


