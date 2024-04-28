def hitung_nilai_akhir(tugas, uts, uas):
    # Menghitung nilai akhir berdasarkan bobot
    nilai_akhir = (0.25 * tugas) + (0.35 * uts) + (0.40 * uas)
    return nilai_akhir

def tentukan_nilai_huruf(nilai_akhir):
    # Menentukan nilai huruf berdasarkan kriteria
    if nilai_akhir > 85:
        return "A"
    elif nilai_akhir > 80:
        return "A-"
    elif nilai_akhir > 75:
        return "B+"
    elif nilai_akhir > 70:
        return "B"
    elif nilai_akhir > 65:
        return "B-"
    elif nilai_akhir > 60:
        return "C+"
    elif nilai_akhir > 55:
        return "C"
    elif nilai_akhir > 50:
        return "C-"
    elif nilai_akhir > 30:
        return "D"
    else:
        return "E"

def main():
    print("Program Menghitung Nilai Akhir Mahasiswa")
    print("=======================================")
    tugas = float(input("Masukkan nilai tugas: "))
    uts = float(input("Masukkan nilai UTS: "))
    uas = float(input("Masukkan nilai UAS: "))

    # Hitung nilai akhir
    nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
    
    # Tentukan nilai huruf
    nilai_huruf = tentukan_nilai_huruf(nilai_akhir)
    
    # Tampilkan hasil
    print(f"Nilai Akhir: {nilai_akhir:.2f}")
    print(f"Nilai Huruf: {nilai_huruf}")

if __name__ == "_main_":
    main()
