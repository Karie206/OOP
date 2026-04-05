#include <iostream>
#include <iomanip>              
#include <string>      
#include <vector>
#include <conio.h>
using namespace std;
             
class CHopDong 
{
	private:
		string maHD;
		string tenNguoiLaoDong;
		long long luongCanBan;
	public:
		CHopDong(string = " ", string = " ", long long = 0);
		CHopDong(const CHopDong&);
		~CHopDong() {};
		void nhap();
		void in();
		friend istream& operator >> (istream&, CHopDong&);
		friend ostream& operator << (ostream&, CHopDong&);
		long long getLuongCanBan();
};

long long CHopDong::getLuongCanBan() 
{
	return luongCanBan; 
}

CHopDong::CHopDong(string maHD, string tenNguoiLaoDong, long long luongCanBan)
{
	this->maHD = maHD;
	this->tenNguoiLaoDong = tenNguoiLaoDong;
	this->luongCanBan = luongCanBan;
}

CHopDong::CHopDong(const CHopDong& temp)
{
	maHD = temp.maHD;
	tenNguoiLaoDong = temp.tenNguoiLaoDong;
	luongCanBan = temp.luongCanBan;
}

void CHopDong::nhap()
{
	cin.ignore();
	cout << "\n- Ma hop dong: "; 
	getline(cin, maHD);
	cout << "- Ten nguoi lao dong: "; 
	getline(cin, tenNguoiLaoDong);
	cout << "- Luong can ban: "; 
	cin >> luongCanBan;
}

void CHopDong::in() 
{
    cout << setw(15) << "|| " + maHD;
    cout << setw(30) << "|| " + tenNguoiLaoDong;
    cout << "|| " << setw(15) << luongCanBan; 
}

istream& operator >> (istream& nhap, CHopDong& temp)
{
	nhap.ignore();
	cout << "\n- Ma hop dong: "; 
	getline(nhap, temp.maHD);
	cout << "- Ten nguoi lao dong: "; 
	getline(nhap, temp.tenNguoiLaoDong);
	cout << "- Luong can ban: "; 
	nhap >> temp.luongCanBan;
	return nhap;
}

ostream& operator << (ostream& in, CHopDong& temp) 
{
	in << setw(15) << "|| " + temp.maHD;
    in << setw(30) << "|| " + temp.tenNguoiLaoDong;
    in << "|| " << setw(15) << temp.luongCanBan; 
    return in;
}

//hop dong ngan han
class CHopDongNganHan : public CHopDong 
{
	private: 
		int thoiHan;
	public:
		CHopDongNganHan(string = " ", string = " ", long long = 0, int = 0);
		CHopDongNganHan(const CHopDongNganHan&);
		void nhap();
		void in();
		friend istream& operator >> (istream&, CHopDongNganHan&);
		friend ostream& operator << (ostream&, CHopDongNganHan&);
		long long luong();
};

CHopDongNganHan::CHopDongNganHan(string maHD, string tenNguoiLaoDong, long long luongCanBan, int thoiHan)
: CHopDong(maHD, tenNguoiLaoDong, luongCanBan)
{
	this->thoiHan = thoiHan;
}

CHopDongNganHan::CHopDongNganHan(const CHopDongNganHan& temp)
: CHopDong(temp)
{
	thoiHan = temp.thoiHan;
}

void CHopDongNganHan::nhap()
{
	CHopDong::nhap();
	cout << "- Thoi han: ";
	cin >> thoiHan;
}

void CHopDongNganHan::in()
{
	CHopDong::in();
	cout << "|| " << setw(12) << thoiHan;
    cout << "|| " << setw(15) << luong();
    cout << "||";
}

istream& operator >> (istream& nhap, CHopDongNganHan& temp)
{
	nhap >> static_cast<CHopDong&>(temp);
	cout << "- Thoi han: ";
	nhap >> temp.thoiHan;
	return nhap;
}

ostream& operator << (ostream& in, CHopDongNganHan& temp)
{
	in << static_cast<CHopDong&>(temp);
	in << "|| " << setw(12) << temp.thoiHan;
    in << "|| " << setw(15) << temp.luong();
    in << "||";
	return in;
}

long long CHopDongNganHan::luong()
{
	return getLuongCanBan();
}

//hop dong dai han
class CHopDongDaiHan : public CHopDong
{
	private:
		long long phuCap;
	public:
		CHopDongDaiHan(string = " ", string = " ", long long = 0, long long = 0);
		CHopDongDaiHan(const CHopDongDaiHan&);
		void nhap();
		void in();
		friend istream& operator >> (istream&, CHopDongDaiHan&);
		friend ostream& operator << (ostream&, CHopDongDaiHan&);
		long long luong();
};

CHopDongDaiHan::CHopDongDaiHan(string maHD, string tenNguoiLaoDong, long long luongCanBan, long long phuCap)
: CHopDong(maHD, tenNguoiLaoDong, luongCanBan)
{
	this->phuCap = phuCap;
}

CHopDongDaiHan::CHopDongDaiHan(const CHopDongDaiHan& temp)
: CHopDong(temp)
{
	phuCap = temp.phuCap;
}

void CHopDongDaiHan::nhap()
{
	CHopDong::nhap();
	cout << "- Phu cap: ";
	cin >> phuCap;
}

void CHopDongDaiHan::in()
{
	CHopDong::in();
	cout << "|| " << setw(12) << phuCap;
	cout << "|| " << setw(15) << luong();
	cout << "||";
}

istream& operator >> (istream& nhap, CHopDongDaiHan& temp)
{
	nhap >> static_cast<CHopDong&>(temp);
	cout << "- Phu cap: ";
	nhap >> temp.phuCap;
	return nhap;
}

ostream& operator << (ostream& in, CHopDongDaiHan& temp)
{
	in << static_cast<CHopDong&>(temp);
	in << "|| " << setw(12) << temp.phuCap;
	in << "|| " << setw(15) << temp.luong();    
	in << "||";
	return in;
}

long long CHopDongDaiHan::luong()
{
	return getLuongCanBan() + phuCap;
}

//quan ly hop dong
class CQuanLyHopDong
{
	private:
		/*
		int soHopDongNH;
		CHopDongNganHan dsHDNH[100];
		
		int soHopDongDH;
		CHopDongDaiHan dsHDDH[100]; 
		*/
		vector<CHopDongNganHan> dsHDNH;
		vector<CHopDongDaiHan> dsHDDH;
	public:
		CQuanLyHopDong();
		void nhapDanhSachHD();
		void inDanhSachHD();
		void tinhTongTienLuong();
		void timHopDongLuongCaoNhat();
		void thucHienChuongTrinh();
};

CQuanLyHopDong::CQuanLyHopDong()
{
	/*
	soHopDongNH = 0;
	soHopDongDH = 0;
	*/
}

void CQuanLyHopDong::nhapDanhSachHD()
{
	int luaChon;
	do
	{
		system("cls");
		cout << "\n+==================================+\n";
   	 	cout << "|      NHAP HOP DONG LAO DONG      |\n";
   	 	cout << "+==================================+\n";
    	cout << "| [1]: Them hop dong ngan han.     |\n";
    	cout << "| [2]: Them hop dong dai han.      |\n";
    	cout << "| [3]: Thoat.                      |\n";
    	cout << "+----------------------------------+\n";
    	cout << "[*] Lua chon cua ban: "; cin >> luaChon;
    	switch(luaChon)
    	{
    		case 1:
    		{
    			CHopDongNganHan temp;
    			cin >> temp; 
    			dsHDNH.push_back(temp);
    			break;
    		}
    		case 2:
    		{
    			CHopDongDaiHan temp;
    			cin >> temp;
    			dsHDDH.push_back(temp);
    			break;
			}
    		case 3:
    		{
    			cout << "\n[!] Thoat...";
				getch();
				break;
			}
			default:
				cout << "\n[!] Lua chon khong hop le, vui long nhap lai...";
				getch();
				break;
		}
	} while(luaChon != 3);
}

void CQuanLyHopDong::inDanhSachHD()
{
	cout << left;
    cout << "\n+================================================================================================+";
    cout << "\n|                                 DANH SACH HOP DONG NGAN HAN                                    |";
    cout << "\n+------------------------------------------------------------------------------------------------+";
    cout << endl;
	cout << setw(15) << "|| Ma HD ";
	cout << setw(30) << "|| Ten nguoi lao dong ";
	cout << setw(18) << "|| Luong can ban ";
	cout << setw(15) << "|| Thoi han ";
	cout << setw(18) << "|| Tong luong ";
	cout << "||" << endl;
	cout << setfill('-') << setw(98) << "-" << endl;
	cout << setfill(' ');
	
	for (int i = 0; i < dsHDNH.size(); i++)
	{
		cout <<	dsHDNH[i];
		cout << endl;
	}
	
	cout << endl;
    cout << "\n+================================================================================================+";
    cout << "\n|                                  DANH SACH HOP DONG DAI HAN                                    |";
    cout << "\n+------------------------------------------------------------------------------------------------+";
    cout << endl;
    cout << setw(15) << "|| Ma HD ";
    cout << setw(30) << "|| Ten nguoi lao dong ";
    cout << setw(18) << "|| Luong can ban ";
    cout << setw(15) << "|| Phu cap ";
    cout << setw(18) << "|| Tong luong ";
    cout << "||" << endl;
    cout << setfill('-') << setw(98) << "-" << endl;
    cout << setfill(' ');
    
    for (int i = 0; i < dsHDDH.size(); i++) 
	{
        cout << dsHDDH[i];
        cout << endl;
    }
    
    cout << "\n[!] Bam phim bat ky de thoat...";
}

void CQuanLyHopDong::tinhTongTienLuong()
{
	long long tongLuongNH = 0;
	long long tongLuongDH = 0;
	
	for (int i = 0; i < dsHDNH.size(); i++)
	{
		tongLuongNH += dsHDNH[i].luong();
	}
	
	for (int i = 0; i < dsHDDH.size(); i++)
	{
		tongLuongDH += dsHDDH[i].luong();
	}
	
	cout << "\n";
	cout << "- Tong tien luong hop dong ngan han: " << tongLuongNH << endl;
	cout << "- Tong tien luong hop dong dai han: " << tongLuongDH << endl;
	cout << "- Tong tien luong tat ca: " << tongLuongNH + tongLuongDH << endl;
	
	cout << "\n[!] Bam phim bat ky de thoat...";
	
}

void CQuanLyHopDong::timHopDongLuongCaoNhat()
{
	if (dsHDNH.size() == 0 && dsHDDH.size() == 0) 
	{
		cout << "\n[!] Danh sach hop dong dang rong...\n";
		cout << "\n[!] Bam phim bat ky de thoat...";
		return;
	}
	
	//hop dong ngan han co luong cao nhat 
	long long maxLuongNH = 0;
	int viTriMaxNH = -1; 
	for (int i = 0; i < dsHDNH.size(); i++)
	{
		if (dsHDNH[i].luong() > maxLuongNH)
		{
			maxLuongNH = dsHDNH[i].luong();
			viTriMaxNH = i;
		}
	}
	
	//hop dong dai han co luong cao nhat
	long long maxLuongDH = 0;
	int viTriMaxDH = -1; 
	for (int i = 0; i < dsHDDH.size(); i++)
	{
		if (dsHDDH[i].luong() > maxLuongDH)
		{
			maxLuongDH = dsHDDH[i].luong();
			viTriMaxDH = i;
		}
	}
	
	cout << "\n+================================================================================================+";
	cout << "\n|                                 HOP DONG CO LUONG CAO NHAT                                     |";
	cout << "\n+------------------------------------------------------------------------------------------------+";
	cout << endl;
	
	if (maxLuongNH > maxLuongDH && viTriMaxNH != -1)
	{
		cout << left;
		cout << setw(15) << "|| Ma HD ";
		cout << setw(30) << "|| Ten nguoi lao dong ";
		cout << setw(18) << "|| Luong can ban ";
		cout << setw(15) << "|| Thoi han ";
		cout << setw(18) << "|| Tong luong ";
		cout << "||" << endl;
		cout << setfill('-') << setw(98) << "-" << endl;
		cout << setfill(' ');
		
		dsHDNH[viTriMaxNH].in();  
		cout << endl;
		
	}
	else if (maxLuongDH > maxLuongNH && viTriMaxDH != -1)
	{
		cout << left;
		cout << setw(15) << "|| Ma HD ";
		cout << setw(30) << "|| Ten nguoi lao dong ";
		cout << setw(18) << "|| Luong can ban ";
		cout << setw(15) << "|| Phu cap ";
		cout << setw(18) << "|| Tong luong ";
		cout << "||" << endl;
		cout << setfill('-') << setw(98) << "-" << endl;
		cout << setfill(' ');
		
		dsHDDH[viTriMaxDH].in();  
		cout << endl;

	}
	cout << "\n[!] Bam phim bat ky de thoat...";
}

void CQuanLyHopDong::thucHienChuongTrinh()
{
	int luaChon;
	do
	{
		system("cls");
		cout << "\n+========================================+\n";
    	cout << "|       QUAN LY HOP DONG LAO DONG        |\n";
    	cout << "+========================================+\n";
    	cout << "| [1]: Nhap danh sach hop dong.          |\n";
    	cout << "| [2]: In danh sach hop dong.            |\n";
    	cout << "| [3]: Tinh tong tien luong.             |\n";
    	cout << "| [4]: Tim hop dong co luong cao nhat.   |\n";
    	cout << "| [5]: Thoat.                            |\n";
    	cout << "+----------------------------------------+\n";
    	cout << "[*] Lua chon cua ban: "; cin >> luaChon;
    	switch(luaChon)
    	{
    		case 1:
    		{
    			nhapDanhSachHD();
    			break;
			}
			case 2:
			{
				inDanhSachHD();
				getch();
				break;
			}
			case 3:
			{
				tinhTongTienLuong();
				getch();
				break;
			}
			case 4:
			{
				timHopDongLuongCaoNhat();
				getch();
				break;
			}
			case 5:
			{
				cout << "\n[!] Cam mon vi da su dung chuong trinh...";
				break;
			}
			default:
				cout << "\n[!] Lua chon khong hop le, vui long nhap lai...";
				getch();
				break;
		}
	} while (luaChon != 5);
}

int main ()
{
	CQuanLyHopDong qlhd;
	qlhd.thucHienChuongTrinh();
	
	return 0;
}
