jadwal_sekolah = {
    "senin": [
        {"jam": "07:30 - 09:00", "mapel": "Upacara & Al-Islam"},
        {"jam": "09:15 - 10:45", "mapel": "Matematika"},
        {"jam": "11:00 - 12:30", "mapel": "Bahasa Indonesia"}
    ],
    "selasa": [
        {"jam": "07:30 - 09:00", "mapel": "Kemuhammadiyahan"},
        {"jam": "09:15 - 10:45", "mapel": "IPA"},
        {"jam": "11:00 - 12:30", "mapel": "Bahasa Inggris"}
    ],
    "rabu": [
        {"jam": "07:30 - 09:00", "mapel": "Pendidikan Agama"},
        {"jam": "09:15 - 10:45", "mapel": "PPKn"},
        {"jam": "11:00 - 12:30", "mapel": "PJOK (Olahraga)"}
    ],
    "kamis": [
        {"jam": "07:30 - 09:00", "mapel": "IPS"},
        {"jam": "09:15 - 10:45", "mapel": "Seni Budaya"},
        {"jam": "11:00 - 12:30", "mapel": "Informatika"}
    ],
    "jumat": [
        {"jam": "07:30 - 09:00", "mapel": "Bahasa Arab"},
        {"jam": "09:15 - 10:30", "mapel": "Prakarya"}
    ]
}

print("=========================================================")
print("   PIMPINAN DAERAH MUHAMMADIYAH BERAU                    ")
print("   SMP MUHAMMADIYAH TANJUNG REDEB                        ")
print("   📚 APLIKASI JADWAL PELAJARAN SEMESTER GENAP 📚       ")
print("=========================================================")

while True:
    print("\nPILIHAN HARI: Senin, Selasa, Rabu, Kamis, Jumat (Ketik 'keluar' untuk selesai)")
    pilihan_hari = input("Masukkan nama hari yang ingin dilihat: ").lower().strip()

    if pilihan_hari == "keluar":
        print("\nTerima kasih! Tetap semangat belajar di SMP Muhammadiyah, Cia! 👋")
        break

    if pilihan_hari in jadwal_sekolah:
        print(f"\n📅 JADWAL PELAJARAN HARI {pilihan_hari.upper()} :")
        print("---------------------------------------------------------")
        for pelajaran in jadwal_sekolah[pilihan_hari]:
            print(f"⏰ {pelajaran['jam']}  ->  📖 {pelajaran['mapel']}")
        print("---------------------------------------------------------")
    else:
        print("❌ Hari tidak valid atau sekolah libur! Periksa kembali tulisanmu ya.")
