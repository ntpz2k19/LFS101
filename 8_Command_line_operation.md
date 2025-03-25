## Command Line Operations

### penggunaan dasar

Berikut penggunaan dasar command line di linux.

 __perintah__ | __fungsi__ | __contoh__
 ---|---|---
 cat  |  menampilkan file | cat file1.txt file2.txt
 head |  menampilkan bagian atas file | head -10 file1.txt
 tail |  menampilkan bagian bawah file | tail -10 file.txt
 more |  menampilkan isi file bertahap dan menurun | more file1.txt
 less |  menampilkan isi file, namun bisa scroll atas dan bawah | apt list --installed &#124; less
 man  |  menampilkan manual dari perintah | man less
 ps   | menampilkan proses | ps aux
 kill | mematikan proses | kill -9 $(pidof firefox)
 pkill | mematikan proses | pkill -U $UID
 shutdown | mematikan komputer | shutdown -h 10:00 "mematikan untuk maintenance"
 which | mencari letak program | which cat
 whereis | mencari letak program, alternatif dari which | which cat
 cd | memindahkan direktori | cd ~ , cd .. , cd .
 pwd | menampilkan direktori yang sedang diakses | pwd



