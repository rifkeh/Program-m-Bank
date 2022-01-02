#include<iostream>
#include<fstream>
using namespace std;
main()
{
	//DEKLARASI
	ifstream Username, Password, Namadepan, Namabelakang, Uang;
	int a, b, c, d, i, j, k, l, m, n, o, p, q;
	int menu, menu2, percobaan, tariktunai, yg, saldo, transferuang, transaksi, menupembayaran;
	int angka, TV, notv, gy, cluster, tahun, noobjek, yatidak;
	string username[255], password[255], namadepan[255], namabelakang[255], transfer, duit[255];
	int uang[255];
	bool x=false;
	bool y=false;
	bool z=false;
	int w;
	bool v=false;
	b=0;
	i=0;
	a=0;
	j=0;
	n=0;
	m=0;
	o=0;
	p=0;
	percobaan=4;
	
	Username.open("Username.txt");			//Membuka file Username.txt
	Password.open("Password.txt");			//Membuka file Password.txt
	Namadepan.open("Nama Depan.txt");		//Membuka file Nama Depan.txt
	Namabelakang.open("Nama Belakang.txt");	//Membuka file Nama Belakang.txt
	Uang.open("uang.txt");
	
	while(!Username.eof())			//Membaca file dari Username dan memasukkan ke username[i]
	{
		Username>>username[i];
		i++;
	}
	
	while(!Password.eof())			//Membaca file dari Password dan memasukkan ke password[b]
	{
		Password>>password[b];
		b++;
	}
	
	while(!Namadepan.eof())			//Membaca file dari Namadepan dan memasukkan ke namadepan[m]
	{
		Namadepan>>namadepan[m];
		m++;
	}
	
	while(!Namabelakang.eof())		//Membaca file dari Namabelakang dan memasukkan ke namabelakang[n]
	{
		Namabelakang>>namabelakang[n];
		n++;
	}
	
	while(!Uang.eof())				//Membaca file dari Uang dan memasukkan ke uang[o]
	{
		Uang>>uang[o];
		o++;
	}
	
	Username.close();				//Menutup file Username.txt
	Password.close();				//Menutup file Password.txt
	Uang.close();					//Menutup file Uang.txt
	
	cout<<"=========== Selamat Datang ============"<<endl;
	cout<<"Silakhan pilih menu"<<endl;
	cout<<"1) Login"<<endl;
	cout<<"2) Register"<<endl;
	cout<<"3) Exit"<<endl;
	cin>>menu;
	system("cls");					//Menghapus bagian atas yang ada di cmd
	switch(menu)
	{
		case 1 : {
		cout<<"================ Login ================"<<endl;
		cout<<"Masukkan username : ";
		cin>>username[i];
		while(!x)								//Melakukan pengecekan apakah username[i] sudah ada yang sama dengan username[j]
		{
			if(username[i]==username[j])
			{
				x=true;
			}else
			{
				if(j==i-1)
				{
					cout<<"Username tidak ada"; 
					cout<<"\nMasukkan username : ";
					cin>>username[i];
					j=0;						
				}else
				{
					j++;
				}
			}
				
		}
		cout<<"Masukkan password : "; 
		cin>>password[i];
		while(x)
		{
			if(password[i]!=password[j])
			{
				cout<<"Password salah\n";
				cout<<"Masukkan password : "; cin>>password[i];
			}else
			{
				x=false;
			}
		}
		system("cls");
		cout<<"Login berhasil!"<<endl<<endl;
		cout<<"Selamat datang, "<<namadepan[j]<<"."<<endl;
		}
		break;
		
		case 2 : 
		{
			j=i-1;
			cout<<"=========== Register ==========="<<endl;
			cout<<"Masukkan nama depan : "; cin>>namadepan[j];
			cout<<"Masukkan nama belakang : "; cin>>namabelakang[j];
			cout<<"Masukkan username : "; cin>>username[j];
		for(c=0; c<j; c++)						//Melakukan pengecekan apakah username yang di register sudah ada yang sama
		{
			while(username[j]==username[c])
			{
				cout<<"Username sudah digunakan"<<endl;
				cout<<"Masukkan username : "; cin>>username[j];
				c=0;
			}
		}
		cout<<"Masukkan password : "; cin>>password[j];
		system("cls");
		cout<<"Akun berhasil dibuat!"<<endl;
		cout<<endl<<"Selamat datang, "<<namadepan[j]<<"."<<endl;
		
		ofstream Username, Password, Namadepan, Namabelakang;
				
		Username.open("Username.txt", ios_base::app);			//Membuka file Username.txt dan melakukan append atau penambahan teks kedalamnya
		Password.open("Password.txt", ios_base::app);			//Membuka file Password.txt dan melakukan append atau penambahan teks kedalamnya
		Namadepan.open("Nama Depan.txt", ios_base::app);		//Membuka file Nama Depan.txt dan melakukan append atau penambahan teks kedalamnya
		Namabelakang.open("Nama Belakang.txt", ios_base::app);	//Membuka file Nama Belakang.txt dan melakukan append atau penambahan teks kedalamnya
		Username<<username[j]<<endl;							//Menambahakan username baru kedalam file Username
		Password<<password[j]<<endl;							//Menambahakan password baru kedalam file Password
		Namadepan<<namadepan[j]<<endl;							//Menambahakan namadepan baru kedalam file Namadepan
		Namabelakang<<namabelakang[j]<<endl;					//Menambahakan namabelakang baru kedalam file Namabelakang
		
		Username.close();
		Password.close();
		Namadepan.close();
		Namabelakang.close();
		break;
		}
		
		case 3 : 
		{
			return 1;				//Ketika diketikkan 3, maka program keluar
		}

	}
	while(!y)						//Untuk masuk kedalam menu terus menerus hingga y true
	{
		cout<<"Saldo di kantung anda : Rp."<<uang[j];
		cout<<"\nSilakhan pilih menu"<<endl;
		cout<<"1) Tarik Tunai"<<endl;
		cout<<"2) Transfer"<<endl;
		cout<<"3) Pembayaran"<<endl;
		cout<<"4) Isi Saldo"<<endl;
		cin>>menu2;
		
		switch(menu2)			//Pembagian situasi berdasarkan menu2
		{
			case 1 : 
			{
				cout<<endl<<"Masukkan nominal uang yang akan anda tarik : Rp."; cin>>tariktunai;
				if(uang[j]-tariktunai<0)
				{
					cout<<endl<<"Saldo anda tidak mencukupi"<<endl;
				}else
				{
					uang[j]=uang[j]-tariktunai;
					ofstream Uang;
					Uang.open("uang.txt");
					for(q=0; q<=i; q++)
					{
						Uang<<uang[q]<<endl;
					}
					Uang.close();
					cout<<"\nTarik tunai berhasil!"<<endl;
				}
				cout<<"\nApakah anda ingin melakukan transaksi kembali?"<<endl;
				cout<<"1)Ya\n2)Tidak"<<endl; cin>>transaksi;
				if(transaksi==2)
				{
					y=true;
				}
				system("cls");
				break;
			}
			case 2 :
			{
				cout<<endl<<"Masukkan tujuan anda transfer (username) : "; cin>>transfer;
				while(!z)
				{
					if(transfer==username[p])
					{
						z=true;
					}
					else
					{
						if(p==i-1)
						{
							cout<<"Tujuan transfer tidak ada"; 
							cout<<"\nMasukkan tujuan anda transfer (username) : ";
							cin>>transfer;
							p=0;
						}
						else
						{
							p++;
						}
					}
				
				}
				cout<<"Masukkan nominal yang anda transfer : "; cin>>transferuang;
				if(uang[j]-transferuang<0)
				{
					cout<<"Saldo anda tidak mencukupi"<<endl;
				}else
				{
					uang[j]=uang[j]-transferuang;
					uang[p]=uang[p]+transferuang;
					ofstream Uang;
					Uang.open("uang.txt");
					for(q=0; q<=i; q++)
					{
						Uang<<uang[q]<<endl;
					}
					Uang.close();
					cout<<endl<<"Transfer berhasil"<<endl;
				}
				cout<<"\nApakah anda ingin melakukan transaksi kembali?"<<endl;
				cout<<"1)Ya\n2)Tidak"<<endl; cin>>transaksi;
				if(transaksi==2)
				{
					y=true;
				}
				system("cls");
				break;
			}
			case 3 : 
			{
				cout<<endl<<"Silakhan pilih menu pembayaran"<<endl;
				cout<<"1) Internet/TV kabel"<<endl;
				cout<<"2) Pajak"<<endl;
				cout<<"3) Listrik"<<endl;
				cout<<"4) PDAM"<<endl;
				cout<<"5) Pendidikan"<<endl;
				cin>>menupembayaran;
				switch(menupembayaran)
				{
					case 1 : 
					{
						cout<<endl<<"Pilih layanan TV kabel/Internet"<<endl;
						cout<<"1) MNC Play"<<endl<<"2) Biznet Home"<<endl<<"3) First Media"<<endl;
						cout<<"4) Indihome"<<endl<<"5) CBN"<<endl<<"6) Kembali"<<endl;
						cin>>TV;
						cout<<"Masukkan nomor layanan TV kabel/Internet : "; cin>>notv;
						cout<<"Biaya dari nomor layanan "<<notv<<" ialah Rp.20.000,00"<<endl;
						cout<<"Apakah anda ingin membayarnya?"<<endl<<"1)Ya\n2)Tidak"; cin>>gy;
						if(gy==1)
						{
							q=0;
							uang[j]=uang[j]-20000;
							ofstream Uang;
							Uang.open("uang.txt");
							for(q=0; q<=i; q++)
							{
								Uang<<uang[q]<<endl;
							}
							Uang.close();
							cout<<"Pembayaran berhasil!";
							break;
						}
					}
					
					
					case 2 : 
					{
						cout<<endl<<"Pilih cluster"<<endl;
						cout<<"1) Jawa Barat"<<endl<<"2) Jawa Timur"<<endl<<"3) Jawa Tengah"<<endl;
						cout<<"4) DKI Jakarta"<<endl<<"5) Riau"<<endl<<"6) Kembali"<<endl;
						cin>>cluster;
						cout<<endl<<"Bayar PBB tahun : "; cin>>tahun;
						cout<<endl<<"Nomor objek pajak : "; cin>>noobjek;
						
						cout<<"Anda akan membayar pajak PBB untuk tahun "<<tahun<<" dengan No objek pajak "<<noobjek<<" sebesar 50000."<<endl;
						cout<<"1)Ya\n2)Tidak"<<endl; 
						cin>>yatidak;
						if(yatidak==1)
						{
							if(uang[j]-50000<0)
							{
								cout<<"Uang anda tidak cukup."<<endl;
							}else
							{
								q=0;
								uang[j]=uang[j]-50000;
								ofstream Uang;
								Uang.open("uang.txt");
								for(q=0; q<=i; q++)
								{
									Uang<<uang[q]<<endl;
								}
								Uang.close();
								cout<<"Pembayaran berhasil!";
							}
							
						}
					}
					
				}
				cout<<"\nApakah anda ingin melakukan transaksi kembali?"<<endl;
				cout<<"1)Ya\n2)Tidak"<<endl; cin>>transaksi;
				if(transaksi==2)
				{
					y=true;
				}
				system("cls");
				break;
			}
				case 4 :
					{
						cout<<endl<<"Pilih metode untuk mengisi saldo"<<endl;
						cout<<"1) Transfer bank"<<endl<<"2) Melalui Alfamart/Indomart"<<endl; cin>>saldo;
						if(saldo==1)
						{
							cout<<"\nSilakhan tranfer melalui bank anda menuju No rekening, 09121639123."<<endl;
							cout<<"Ketik 1 jika sudah melakukan tranfer dan 2 untuk membatalkan."<<endl;
							cin>>angka;
							if(angka==1)
							{
								q=0;
								uang[j]=uang[j]+50000;
								ofstream Uang;
								Uang.open("uang.txt");
								for(q=0; q<=i; q++)
								{
									Uang<<uang[q]<<endl;
								}
								Uang.close();
								cout<<"Isi Saldo berhasil!"<<endl;
							}
						}
						else
						{
							cout<<"\nSilakhan tranfer melalui Alfamart/Indomart dan tunjukkan No rekening 09121639123 kepada kasir."<<endl;
							cout<<"Ketik 1 jika sudah melakukan tranfer dan 2 untuk membatalkan."<<endl;
							cin>>angka;
							if(angka==1)
							{
								q=0;
								uang[j]=uang[j]+50000;
								ofstream Uang;
								Uang.open("uang.txt");
								for(q=0; q<=i; q++)
								{
									Uang<<uang[q]<<endl;
								}
								Uang.close();
								cout<<"Isi Saldo berhasil!"<<endl;
							}
						}
						cout<<"\nApakah anda ingin melakukan transaksi kembali?"<<endl;
						cout<<"1)Ya\n2)Tidak"<<endl; cin>>transaksi;
						if(transaksi==2)
						{
							y=true;
						}
						system("cls");
						break;
						
					}
			
			
			}
		}
		
	}
