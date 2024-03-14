# tugas1_struktur_data_kel11
Penerapan Linked List pada Pemesanan Mixue

# Tugas Struktur Data 1 - Mixue

class Pesanan:
    def __init__(self, nama_menu, harga, jumlah=1, next=None):
        self.nama_menu = nama_menu
        self.harga = harga
        self.jumlah = jumlah
        self.next = next

class DaftarPesanan:
    def __init__(self):
        self.head = None
    
    def tambahkan_pesanan(self, nama_menu, harga, jumlah):
        pesanan = Pesanan(nama_menu, harga, jumlah)

        if self.head is None:
            self.head = pesanan
            return

        temp = self.head
        while (temp.next):
            temp = temp.next

        temp.next = pesanan
    
    def print(self):
        if self.head is None:
            print("Daftar Pesanan masih Kosong")
            return

       pesanan = self.head
        while pesanan:
            print(f"{pesanan.nama_menu}: {pesanan.harga}: {pesanan.jumlah}: - {pesanan.harga*pesanan.jumlah}: rupiah")
            pesanan = pesanan.next
    
    def total_pesanan(self):
        total = 0
        
        pesanan = self.head
        while pesanan:
            total += pesanan.harga * pesanan.jumlah
            pesanan = pesanan.next
        
        print(f"Total Harga Pesanan: Rp{total}")

daftar_pesanan = DaftarPesanan()

# menu dan harga 
MENU = [
    ["Mixue Ice Cream", 5_000], 
    ["Mi Sundae", 14_000], 
    ["Boba Shake", 16_000], 
    ["Mi ganas", 11_000], 
    ["Creamy Manggo Boba", 22_000]
    ] 


print(
"""
1. Mixue Ice Cream: 5000
2. Mi Sundae:14000
3. Boba Shake:16000
