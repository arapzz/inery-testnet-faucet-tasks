# Inery testnet faucet tasks

This is the base branch for tasks related to the Inery faucet. For each task that requires revision using GitHub, we will create a new branch named with the number of that task, such as 'task4', 'task5', etc.

## Getting Started

To verify the quality of your code, you will need to clone the specific branch of the project and submit the required changes for that task. After making the necessary changes, you can create a pull request to submit your work for review. If the work is satisfactory, it will be approved. If there are any issues with the work, it may be labeled with specific comments indicating what needs to be improved or modified. It is important to carefully review and address any feedback provided in order to improve the quality of your work.


## INERY TASK 4 add repo inery-blockchain/inery-testnet-faucet-tasks ##

🌐 Tetapkan nama akun sebagai variabel env dan Set PATH env
Agar tidak berulang menulis nama Akun Inery, kita perlu mengatur nama akun sebagai Variable env, silahkan ganti Nama_Akun_Inery dengan Nama Akun Inerymu

```
IneryAccname=Nama_Akun_Inery
export PATH="$PATH:$HOME/inery.cdt/bin:$HOME/inery-node/inery/bin"
```

🌐 Membuat Proyek Tugas Frok
Kunjungi Halaman : https://github.com/inery-blockchain/inery-testnet-faucet-tasks

Klik tanda panah ke bawah di samping tulisan Fork dan klik Create a new fork dan lanjutkan membuat frok

Membuat klon

Klik Code dan Copy link clone dan, jangan lupa <link_clone> ganti dengan link yang kamu copy tadi dan buang tanda lanjutkan <>

```
cd
git clone <link_clone>
```

Membuat proyek direktori

```
cd ~/inery-testnet-faucet-tasks
mkdir $IneryAccname
```

🌐 Jalankan Perintah Build-Web:

```
cd ~/ineryjs
npm run build-web
```

🌐 mengcopy Folder disit-web ke Project

```
cp -r $HOME/ineryjs/dist-web/ $HOME/inery-testnet-faucet-tasks/$IneryAccname/dist-web/
```

> (COMMAND INI YANG KURANG DI VIDEO JADI LANJUTIN MASIH DI DIREKTORI INERYJS)

JIKA SUDAH, LANJUT COMMAND BERIKUT

```
cd ~/inery-testnet-faucet-tasks/$IneryAccname
nano index.html
```

Masukan Script di bawah ini dan jangan lupa ganti IPmu serta buang tanda <>

```
<script src="./dist-web/inery-jsonrpc.min.js"></script>
<script src="./dist-web/inery-api.min.js"></script>
<script src="./dist-web/inery-jssig.min.js"></script>
<script>
    (async()=>{
        const rpc=new ineryjs_jsonrpc.JsonRpc("https://<IPmu>:8888");
        console.log(await rpc.get_info());
    })();
</script>
```

🌐 Membuat Tutorial (bisa diskip bagian ini kalau ragu dengan tasknya)
Silahkan buat tutorial mengenai Inery sebagai bagian dari Solution Project

```
cd ~/inery-testnet-faucet-tasks/$IneryAccname
nano README.md
```

🌐 Menghubungkan Task ke Github

```
cd ~/inery-testnet-faucet-tasks/
git add $IneryAccname/
git add .
git commit -m "task 4 solution inery : $IneryAccname"
git branch -M main
git push -u origin main
```

🌐 Kembali lagi ke Github
Silahkan Refresh repository Fork yang dibuat di step 2 tadi, lalu klik commit kedepan

Lanjutkan Buat permintaan tarik

Cek hasilnya di https://github.com/inery-blockchain/inery-testnet-faucet-tasks
