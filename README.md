class Murid:
    def __init__(self, nama, usia, alamat):
        self.nama = nama
        self.usia = usia
        self.alamat = alamat

    def info(self):
        print(f"Nama: {self.nama}")
        print(f"Usia: {self.usia}")
        print(f"Alamat: {self.alamat}")

murid_list = []

def daftar_sekolah():
    print("=== Pendaftaran Sekolah ===")
    nama = input("Masukkan nama: ")
    usia = input("Masukkan usia: ")
    alamat = input("Masukkan alamat: ")
    murid_baru = Murid(nama, usia, alamat)
    murid_list.append(murid_baru)
    print("Pendaftaran berhasil!")

def tampilkan_murid():
    print("\n=== Daftar Murid ===")
    for index, murid in enumerate(murid_list, start=1):
        print(f"Murid {index}:")
        murid.info()
        print()

# Menu Utama
while True:
    print("\n=== MENU ===")
    print("1. Daftar Sekolah")
    print("2. Tampilkan Murid")
    print("3. Keluar")

    pilihan = input("Pilih menu: ")

    if pilihan == '1':
        daftar_sekolah()
    elif pilihan == '2':
        tampilkan_murid()
    elif pilihan == '3':
        print("Terima kasih!")
        break
    else:
        print("Pilihan tidak valid. Silakan pilih kembali.")
