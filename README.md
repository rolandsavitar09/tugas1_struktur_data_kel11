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

            
