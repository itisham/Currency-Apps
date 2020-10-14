# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah. Satu dollar dianggap senilai Rp.15.000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info "INVALID" jika yang dimasukkan berupa text

## How Does It Works?
Diawali method `MainWindow` pada class `MainWindow.xaml.cs`, kita mendeklarasikan `InitializeComponent` dan membuat objek dari class `CurrencyController.cs`

```csharp
   public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
```

Logika perhitungan terdapat pada class `CurrencyController.cs` sebagai berikut cara kerjanya yaitu

-  Mendeklarasikan variabel `nominalDouble` yang berisi variabel `nominal` yang telah diconvert menjadi double
-  Mendeklarasikan variabel `result` yang berisi variabel `nominalDouble * 15000`
-  Nilai dari variabel `result` diconvert menjadi string dan dikembalikan ke nominal 

```csharp
    public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```