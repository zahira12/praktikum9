# praktikum9

# Latihan1# Menentukan Nilai Max dan Min dari n bilangan bulat menggunakan array

	~Alur algoritmanya
	-Mendeklarasikan public int proses(int n,int max, int min, int jumlah);
	-Mendeklarasikan private int n, max, min, jumlah, x;
	-Menampilkan maximum, minimum, dan jumlah deret
	-Masukan bilangan cout<<" Masukkan Bilangan : ";cin>>x;
			      jumlah+=x;

			   if(x<min)
			   {
			      min=x;
			   }

			   if(x>max)
			   {
			      max=x;
			   }
			    return proses(n-1,max,min,jumlah);
			   }
	-Mencetak hasil 	int main(int argc, char *argv[]){
				    maxmin x;
				    x.proses(5,1,1,0);

				    system("PAUSE");

				    return EXIT_SUCCESS;
				}	


~Berikut kode Lengkapnya

	#include <iostream>
	#include <cstdlib>

	/* run this program using the console pauser or add your own getch, system("pause") or input loop */

	using namespace std;

	class maxmin
	  {
	   public:
	          maxmin();
	          int proses(int n,int max,int min,int jumlah);
	   private:
	          int n, max, min, jumlah, x;
	  };

	maxmin::maxmin()
	{
	  cout<<"\tMenampilkan Maximum, Minimum, dan Jumlah Seluruh Deret "<<endl;
	  cout<<endl;
	}

	int maxmin::proses(int n, int max, int min, int jumlah)
	{
	if(n==0){
	   cout<<endl;
	   cout<<" NILAI MAKSIMUM       : "<<max<<endl;
	   cout<<" NILAI MINIMUM        : "<<min<<endl;
	   cout<<" JUMLAH SELURUH DERET : "<<jumlah<<endl<<endl;
	   return 0;
	  }

	else{
	   cout<<" Masukkan Bilangan : ";cin>>x;
	      jumlah+=x;

	   if(x<min)
	   {
	      min=x;
	   }

	   if(x>max)
	   {
	      max=x;
	   }
	    return proses(n-1,max,min,jumlah);
	 }
	}

	int main(int argc, char *argv[]){
	    maxmin x;
	    x.proses(5,1,1,0);

	    system("PAUSE");

	    return EXIT_SUCCESS;
	}


~Berikut hasil Screenshotnya
![img](https://github.com/zahira12/praktikum9/blob/master/latihan1/HasilScreenshot1.png)

# Latihan2# Menentukan Modus dari n buah bilangan bulat

	~Alur algoritmanya
	-Menentukan Modus dari n buah bilangan bulat
	-Mendeklarasikan int x;
			 int findmod(float bil[], int n, float mod[])
			 {
			 int total[100];
			 int k=1;
			 x=0;
	-Mengurutkan secara ascending
			for(int c=0;c<n;c++)
			{
			for(int i=(n-1);i>=0;i--)
			{
			if(bil[i]<bil[i-1])
			{
			int temp;
			temp=bil[i];
			bil[i]=bil[i-1];
			bil[i-1]=temp;
			}
	-Menghitung berapa kali muncul tiap angka
	-Menentukan nilai yang paling sering muncul
	-Cetak hasilnya cout<<"\nBanyak data N : ";cin>>n;
			for(int c=0;c<n;c++)
			{
			cout<<"Nilai "<<(c+1)<<" : ";cin>>bil[c];
			}
			cout<<endl;
			findmod(bil,n,mod);
			if (x==0)


~Berikut kode Lengkapnya

	#include <iostream>
	#include<conio.h>

	using namespace std;

	int x;
	int findmod(float bil[], int n, float mod[])
	{
	int total[100];
	int k=1;
	x=0;
	//untuk mengurutkan secara ascending
	for(int c=0;c<n;c++)
	{
	for(int i=(n-1);i>=0;i--)
	{
	if(bil[i]<bil[i-1])
	{
	int temp;
	temp=bil[i];
	bil[i]=bil[i-1];
	bil[i-1]=temp;
	}
	}
	}
	//menghitung berapa kali muncul tiap angka
	for(int c=0;c<n;c++)
	{
	total[c]=0;
	for(int i=0;i<n;i++)
	{
	if(bil[c]==bil[i])
	{
	total[c]++;
	}
	}
	}
	//menentukan nilai yang paling sering muncul
	for(int c=0;c<n;c++)
	{
	if(total[c]>k)
	{
	k=total[c];
	}
	}
	//jika modus lebih dari satu
	for(int c=0;c<n;c++)
	{
	if(x==0)
	mod[x]=0;
	else
	mod[x]=mod[x-1];
	if(total[c]==k)
	{
	if(bil[c]!=mod[x])
	{
	mod[x]=bil[c];
	x++;
	}
	}
	}

	//Jika Semua angka muncul sama banyak
	int z=0;
	for(int c=0;c<n;c++)
	{
	if(total[c]==k)
	{
	z++;
	}
	}
	if(z==n)
	{
	x=0;
	}
	}
	int main()
	{
	int n;
	float bil[100];
	float mod[100];
	cout<<"=================="<<endl;;
	cout<<"Nilai MODUS"<<endl;
	cout<<"=================="<<endl;
	cout<<"\nBanyak data N : ";cin>>n;
	for(int c=0;c<n;c++)
	{
	cout<<"Nilai "<<(c+1)<<" : ";cin>>bil[c];
	}
	cout<<endl;
	findmod(bil,n,mod);
	if (x==0)
	cout<<"Tidak Ada Modus!"<<endl;
	else
	{
	cout<<"Modus : ";
	for(int c=0;c<x;c++)
	{
	cout<<mod[c]<<" ";
	}
	}
	getch();
	}


~Berikut hasil Screenshotnya
![img](https://github.com/zahira12/praktikum9/blob/master/latihan2/HasilScreenshot2.png)

# Latihan3# Program untuk mengalikan dua buah matriks

	~Alur algoritmanya
	-Membuat program untuk mengalikan dua buah matriks
	-Mendeklarasikan void baca_matriks (int mat[10][10], int baris, int kolom)
	-Mendelarasikan  void proses( int x[10][10],const int matriks1[10][10],const int matriks2[10][10], int baris, int kolom){
	-Cetak 		 void cetak_matriks (const int A[10][10], int baris, int kolom)
	-Masukkan	 int matriks1[10][10], matriks2[10][10];
			 int x[10][10];
	-Cetak hasilnya  cout << "Data matriks ke-1\n";
			 baca_matriks(matriks1,m,n);
			 cetak_matriks(matriks1,m,n);
			 cout << "Data matriks ke-2\n";
			 baca_matriks(matriks2,m,n);
			 cetak_matriks(matriks2,m,n);
			 proses(x,matriks1,matriks2,m,n);
			 cout << "Hasil Perkalian : \n";
			 cetak_matriks(x,m,n);
			 }

~Berikut kode Lengkapnya

	#include <iostream>
	using namespace std;

	void baca_matriks (int mat[10][10], int baris, int kolom)
	{ int i,j;
	for (i=0; i<baris; i++)
	for (j=0; j<kolom; j++)
	{ cout << "Data [" << i+1 << "," << j+1 << "] : ";
	cin >> mat[i][j];
	}
	}

	void proses( int x[10][10],const int matriks1[10][10],const int matriks2[10][10], int baris, int kolom){
	for(int i=0;i<baris;i++)
	for(int j=0;j<kolom;j++)
	 {
	  x[i][j]=0;
	  for(int k=0;k<kolom;k++)
	  x[i][j]=x[i][j]+matriks1[i][k]*matriks2[k][j];

	}
	}
	void cetak_matriks (const int A[10][10], int baris, int kolom)
	{ int i,j;
	for (i=0; i<baris; i++)
	{ for (j=0; j<kolom; j++)
	cout << A[i][j]<<" ";
	cout << endl;
	}
	}
	 main() {
	int m, n;
	int matriks1[10][10], matriks2[10][10];
	int x[10][10];
	cout << "Banyak baris : ";
	cin >> m;
	cout << "Banyak kolom : ";
	cin >> n;
	cout << "Data matriks ke-1\n";
	baca_matriks(matriks1,m,n);
	cetak_matriks(matriks1,m,n);
	cout << "Data matriks ke-2\n";
	baca_matriks(matriks2,m,n);
	cetak_matriks(matriks2,m,n);
	proses(x,matriks1,matriks2,m,n);
	cout << "Hasil Perkalian : \n";
	cetak_matriks(x,m,n);
	}


~Berikut hasil Screenshotnya
![img](https://github.com/zahira12/praktikum9/blob/master/latihan3/hasilscreenshot3.png)

# Latihan4# Program untuk menghasilkan Transpose suatu matriks

	~Alur algoritmanya
	-Membuat program untuk menghasilkan transpose seuatu matriks
	-Mendeklarasikan int main(int argc, char *argv[])
	-Masukkan int a[10][10],m,n,i,j;
		  cout<<"Masukkan Jumlah Baris: ";
		  cin>>m;
		  cout<<"Masukkan Jumlah kolom: ";
		  cin>>n;
	-Cetak    cout<<endl<<"Elemen matriks: "<<endl;
		  cout<<"masukkan elemen a: "<<i+1<<j+1<<": ";
		  cin>>a[i][j];
		  cout<<endl<<"Matriks: "<<endl<<endl;
		  cout<<endl<<"Transpose Matriks: "<<endl<<endl;

~Berikut kode Lengkapnya

	#include <cstdlib>
	#include <iostream>

	using namespace std;

	int main(int argc, char *argv[])
	{

	int a[10][10],m,n,i,j;
	cout<<"Masukkan Jumlah Baris: ";
	cin>>m;
	cout<<"Masukkan Jumlah kolom: ";
	cin>>n;


	cout<<endl<<"Elemen matriks: "<<endl;
	for(i=0;i<m;i++)
	{
	for(j=0;j<n;j++)
	{
	cout<<"masukkan elemen a: "<<i+1<<j+1<<": ";
	cin>>a[i][j];
	}
	}
	cout<<endl<<"Matriks: "<<endl<<endl;
	for(i=0;i<m;i++)
	{
	for(j=0;j<n;j++)
	{
	cout<<a[i][j]<<" ";
	}
	cout<<endl<<endl;
	}
	cout<<endl<<"Transpose Matriks: "<<endl<<endl;
	for(i=0;i<m;i++)
	{
	for(j=0;j<n;j++)
	{
	cout<<a[j][i]<<" ";
	}
	cout<<endl<<endl;
	}

	system("PAUSE");
	return EXIT_SUCCESS;
	}


~Berikut hasil Screenshotnya
![img](https://github.com/zahira12/praktikum9/blob/master/latihan4/hasilscreenshot4.png)

~flowchart

![img](https://github.com/zahira12/praktikum9/blob/master/flowchart.png)
