import tkinter as tk


master_jadwal = { 
    "senin": { 
        "VII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:45", "mapel": "PJOK"}, {"jam": "09:45 - 10:25", "mapel": "Kemuhammadiyahan"}, {"jam": "10:40 - 11:55", "mapel": "Matematika"}, {"jam": "12:30 - 14:30", "mapel": "IPA"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:45", "mapel": "PJOK"}, {"jam": "09:45 - 11:55", "mapel": "IPA"}, {"jam": "12:30 - 14:30", "mapel": "Seni Budaya"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:05", "mapel": "IPS"}, {"jam": "09:05 - 10:25", "mapel": "Informatika"}, {"jam": "10:40 - 11:55", "mapel": "Bahasa Indonesia"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:05", "mapel": "Matematika"}, {"jam": "09:05 - 10:25", "mapel": "Informatika"}, {"jam": "10:40 - 11:55", "mapel": "Bahasa Arab"}, {"jam": "12:30 - 14:30", "mapel": "Bahasa Indonesia"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:45", "mapel": "Tajwid"}, {"jam": "09:45 - 11:55", "mapel": "Murojaah / Hafalan"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:45", "mapel": "MBA"}, {"jam": "09:45 - 11:55", "mapel": "Murojaah / Hafalan"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:45", "mapel": "MBA"}, {"jam": "09:45 - 11:55", "mapel": "Murojaah / Hafalan"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha / Pembinaan Walas"}, {"jam": "07:30 - 07:45", "mapel": "Literasi"}, {"jam": "07:45 - 09:05", "mapel": "Bahasa Indonesia"}, {"jam": "09:05 - 10:25", "mapel": "Pend. Pancasila"}, {"jam": "10:40 - 11:55", "mapel": "Pend. Pancasila"}, {"jam": "12:30 - 14:30", "mapel": "Kemuhammadiyahan"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ] 
    }, 
    "selasa": { 
        "VII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "PAI"}, {"jam": "09:30 - 11:50", "mapel": "Matematika"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "IPS"}, {"jam": "08:50 - 10:10", "mapel": "Bahasa Indonesia"}, {"jam": "10:30 - 11:50", "mapel": "Bahasa Inggris"}, {"jam": "12:30 - 13:10", "mapel": "Bahasa Arab"}, {"jam": "13:10 - 14:30", "mapel": "Informatika"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "Seni Budaya"}, {"jam": "08:50 - 10:10", "mapel": "PAI"}, {"jam": "10:30 - 11:50", "mapel": "IPA"}, {"jam": "12:30 - 14:30", "mapel": "Informatika"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "PAI"}, {"jam": "08:50 - 10:10", "mapel": "PAI"}, {"jam": "10:30 - 11:50", "mapel": "Kemuhammadiyahan"}, {"jam": "12:30 - 14:30", "mapel": "Informatika"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "PJOK"}, {"jam": "09:30 - 10:10", "mapel": "PAI"}, {"jam": "10:30 - 11:50", "mapel": "Tahsin"}, {"jam": "12:30 - 14:30", "mapel": "Kemuhammadiyahan"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "PJOK"}, {"jam": "09:30 - 10:10", "mapel": "PAI"}, {"jam": "10:30 - 11:50", "mapel": "Tahsin"}, {"jam": "12:30 - 14:30", "mapel": "Seni Budaya"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "PJOK"}, {"jam": "09:30 - 10:10", "mapel": "PAI"}, {"jam": "10:30 - 11:50", "mapel": "Tahsin"}, {"jam": "12:30 - 14:30", "mapel": "Seni Budaya"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "Prakarya"}, {"jam": "08:50 - 09:30", "mapel": "IPS"}, {"jam": "10:30 - 11:50", "mapel": "Bahasa Indonesia"}, {"jam": "12:30 - 14:30", "mapel": "PAI"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ] 
    }, 
    "rabu": { 
        "VII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "Bahasa Inggris"}, {"jam": "08:50 - 10:10", "mapel": "Bahasa Indonesia"}, {"jam": "10:30 - 11:50", "mapel": "IPS"}, {"jam": "12:30 - 13:10", "mapel": "Bahasa Arab"}, {"jam": "13:10 - 14:30", "mapel": "IPA"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 10:10", "mapel": "Pend. Pancasila"}, {"jam": "10:30 - 11:50", "mapel": "Bahasa Indonesia"}, {"jam": "12:30 - 14:30", "mapel": "PAI"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "IPS"}, {"jam": "08:50 - 10:10", "mapel": "Informatika"}, {"jam": "10:30 - 11:50", "mapel": "Matematika"}, {"jam": "12:30 - 14:30", "mapel": "Matematika"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "Informatika"}, {"jam": "08:50 - 10:10", "mapel": "PAI"}, {"jam": "10:30 - 11:50", "mapel": "Matematika"}, {"jam": "12:30 - 14:30", "mapel": "Matematika"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 10:10", "mapel": "Tajwid"}, {"jam": "10:30 - 11:50", "mapel": "Tahsin"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 10:10", "mapel": "Tajwid"}, {"jam": "10:30 - 11:50", "mapel": "Tahsin"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 10:10", "mapel": "Tajwid"}, {"jam": "10:30 - 11:50", "mapel": "Tahsin"}, {"jam": "12:30 - 14:30", "mapel": "Pend. Pancasila"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 10:10", "mapel": "IPA (Biologi)"}, {"jam": "10:30 - 11:50", "mapel": "Bahasa Inggris"}, {"jam": "12:30 - 14:30", "mapel": "Bahasa Indonesia"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ] 
    }, 
    "kamis": { 
        "VII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "Seni Budaya"}, {"jam": "09:30 - 10:10", "mapel": "Kemuhammadiyahan"}, {"jam": "10:30 - 11:50", "mapel": "Bahasa Indonesia"}, {"jam": "12:30 - 13:50", "mapel": "IPS"}, {"jam": "13:50 - 14:30", "mapel": "Bahasa Arab"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:10", "mapel": "Bahasa Arab"}, {"jam": "08:10 - 10:10", "mapel": "Matematika"}, {"jam": "10:30 - 11:50", "mapel": "IPS"}, {"jam": "12:30 - 13:50", "mapel": "IPA"}, {"jam": "13:50 - 14:30", "mapel": "Kemuhammadiyahan"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII A": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "IPS"}, {"jam": "08:50 - 10:10", "mapel": "Bahasa Inggris"}, {"jam": "10:30 - 11:50", "mapel": "Matematika"}, {"jam": "12:30 - 13:50", "mapel": "Kemuhammadiyahan"}, {"jam": "13:50 - 14:30", "mapel": "Bahasa Indonesia"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII B": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 08:50", "mapel": "Bahasa Indonesia"}, {"jam": "08:50 - 10:10", "mapel": "Bahasa Inggris"}, {"jam": "10:30 - 11:50", "mapel": "Matematika"}, {"jam": "12:30 - 13:50", "mapel": "Seni Budaya"}, {"jam": "13:50 - 14:30", "mapel": "Seni Budaya"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "Tajwid"}, {"jam": "09:30 - 10:10", "mapel": "Murojaah / Hafalan"}, {"jam": "10:30 - 11:50", "mapel": "Murojaah / Hafalan"}, {"jam": "12:30 - 13:50", "mapel": "Seni Budaya"}, {"jam": "13:50 - 14:30", "mapel": "IPS"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "VIII TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "Tajwid"}, {"jam": "09:30 - 10:10", "mapel": "Murojaah / Hafalan"}, {"jam": "10:30 - 11:50", "mapel": "Murojaah / Hafalan"}, {"jam": "12:30 - 13:50", "mapel": "Informatika"}, {"jam": "13:50 - 14:30", "mapel": "IPS"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX TAHFIZ": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "Al-Qur'an Hadist"}, {"jam": "09:30 - 10:10", "mapel": "Murojaah / Hafalan"}, {"jam": "10:30 - 11:50", "mapel": "Murojaah / Hafalan"}, {"jam": "12:30 - 13:50", "mapel": "Prakarya"}, {"jam": "13:50 - 14:30", "mapel": "IPS"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ], 
        "IX": [ {"jam": "07:15 - 07:30", "mapel": "Sholat Dhuha & Bina Islam"}, {"jam": "07:30 - 09:30", "mapel": "PJOK"}, {"jam": "09:30 - 10:10", "mapel": "Seni Budaya"}, {"jam": "10:30 - 11:50", "mapel": "Seni Budaya"}, {"jam": "12:30 - 13:50", "mapel": "Bahasa Arab"}, {"jam": "13:50 - 14:30", "mapel": "Bahasa Inggris"}, {"jam": "14:30 - 15:30", "mapel": "TPA"} ] 
    }, 
    "jumat": { 
        "VII A": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:00", "mapel": "Bahasa Inggris"}, {"jam": "10:00 - 10:40", "mapel": "Bahasa Indonesia"}, {"jam": "10:40 - 11:15", "mapel": "Informatika"} ], 
        "VII B": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:00", "mapel": "Matematika"}, {"jam": "10:00 - 10:40", "mapel": "Bahasa Inggris"}, {"jam": "10:40 - 11:15", "mapel": "Bahasa Indonesia"} ], 
        "VIII A": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:00", "mapel": "Kemuhammadiyahan"}, {"jam": "10:00 - 10:40", "mapel": "Informatika"}, {"jam": "10:40 - 11:15", "mapel": "IPA"} ], 
        "VIII B": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:00", "mapel": "Bahasa Indonesia"}, {"jam": "10:00 - 10:40", "mapel": "Informatika"}, {"jam": "10:40 - 11:15", "mapel": "Pend. Pancasila"} ], 
        "VII TAHFIZ": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:40", "mapel": "Tahsin"}, {"jam": "10:40 - 11:15", "mapel": "PAI"} ], 
        "VIII TAHFIZ": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:40", "mapel": "Tahsin"}, {"jam": "10:40 - 11:15", "mapel": "PAI"} ], 
        "IX TAHFIZ": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:40", "mapel": "Tahsin"}, {"jam": "10:40 - 11:15", "mapel": "IPA (Fisika)"} ], 
        "IX": [ {"jam": "07:00 - 07:30", "mapel": "Literasi / Senam"}, {"jam": "07:30 - 09:00", "mapel": "Tapak Suci"}, {"jam": "09:20 - 10:00", "mapel": "IPS"}, {"jam": "10:00 - 10:40", "mapel": "Matematika"}, {"jam": "10:40 - 11:15", "mapel": "IPA (Fisika)"} ] 
    } 
}


jendela = tk.Tk()
jendela.title("Aplikasi Jadwal Pelajaran Akbar - SMP Muhammadiyah Tanjung Redeb")
jendela.geometry("680x580")

hari_aktif = "senin"

def update_jadwal():
    kelas_aktif = variabel_kelas.get()
    
   
    label_status.config(text=f"📌 JADWAL AKTIF ➡️ HARI: {hari_aktif.upper()} | KELAS: {kelas_aktif}")
    
   
    hari_data = master_jadwal.get(hari_aktif, {})
    list_pelajaran = hari_data.get(kelas_aktif, [])
    
   
    teks_tampilan = ""
    if list_pelajaran:
        for idx, pelajaran in enumerate(list_pelajaran, 1):
            teks_tampilan += f"{idx}. ⏰ {pelajaran['jam']}   ->   📖 {pelajaran['mapel']}\n\n"
    else:
        teks_tampilan = "❌ Jadwal belum tersedia atau hari libur!"

  
    kotak_jadwal.config(state=tk.NORMAL)
    kotak_jadwal.delete("1.0", tk.END)
    kotak_jadwal.insert(tk.END, teks_tampilan)
    kotak_jadwal.config(state=tk.DISABLED)

def hari_dipilih(nama_hari):
    global hari_aktif
    hari_aktif = nama_hari
    update_jadwal()

def kelas_dipilih(pilihan_kelas):
    update_jadwal()


judul_sekolah = tk.Label(jendela, text="SMP MUHAMMADIYAH TANJUNG REDEB", font=("Arial", 14, "bold"), fg="#1e4d2b")
judul_sekolah.pack(pady=(15, 2))
judul_sub = tk.Label(jendela, text="Aplikasi Jadwal Pelajaran Akbar (Semua Kelas)", font=("Arial", 10, "italic"))
judul_sub.pack(pady=(0, 15))


wadah_tombol = tk.Frame(jendela)
wadah_tombol.pack(pady=5)

hari_list = ["senin", "selasa", "rabu", "kamis", "jumat"]
for h in hari_list:
    btn = tk.Button(wadah_tombol, text=h.upper(), width=9, font=("Arial", 9, "bold"),
                    command=lambda hari=h: hari_dipilih(hari), bg="#f0f0f0")
    btn.pack(side=tk.LEFT, padx=5)


judul_kelas = tk.Label(jendela, text="Pilih Kelas:", font=("Arial", 11, "bold"))
judul_kelas.pack(pady=(15, 2))

daftar_kelas = ["VII A", "VII B", "VIII A", "VIII B", "VII TAHFIZ", "VIII TAHFIZ", "IX TAHFIZ", "IX"]
variabel_kelas = tk.StringVar(jendela)
variabel_kelas.set(daftar_kelas[0]) 

menu_kelas = tk.OptionMenu(jendela, variabel_kelas, *daftar_kelas, command=kelas_dipilih)
menu_kelas.config(width=15, font=("Arial", 10))
menu_kelas.pack(pady=5)


label_status = tk.Label(jendela, text="", font=("Arial", 11, "bold"), fg="darkblue")
label_status.pack(pady=(20, 5))


kotak_jadwal = tk.Text(jendela, width=65, height=12, font=("Helvetica", 11), bg="#fefefe", padx=15, pady=15)
kotak_jadwal.pack(pady=10)


update_jadwal()

jendela.mainloop()
