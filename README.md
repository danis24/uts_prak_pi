# UTS PRAKTIKUM PEMPROGRAMAN INTERNET (PI)

### Rules

ada beberapa aturan yang harus temen-temen pahami dalam pengerjaan UTS ini di antaranya :

* UTS di kerjakan secara takehome.
* UTS di kerjakan bebas mencari referensi darimana saja.
* UTS tidak boleh kerjasama dengan teman lainnya
* UTS di tulis dengan menggunakan bahasa PHP OOP

Sebelum masuk ke soal peserta UTS di haruskan menyiapkan environment terlebih dahulu di antaranya :

* Database : uts_db
* Table: users

```
create table users(
    id int primary key auto_increment,
    first_name varchar(30),
    last_name varchar(30),
    username varchar(20),
    email varchar(30),
    password varchar(75)
);
```

* table : categories

```
create table categories(
    id int primary key auto_increment,
    name varchar(30),
    description text
);
```

* Table : books

```
create table books(
    id int primary key auto_increment,
    serial varchar(20),
    title varchar(30),
    author varchar(45),
    synopsis text,
    id_books_categories int
);
```

### SOAL

1. Buatlah aplikasi CRUD dengan menggunakan koneksi MySQL dan PHP OOP dari struktur table di atas!
2. Buatlah sesuai dengan struktur database di atas!

### KETERANGAN

* untuk tampilan bebas menggunakan HTML/CSS/Bootstrap asalkan tidak nenggunakan template

- hasil uts di upload ke akun github masing-masing
- di kumpulkan dalam bentuk link repository github ke email danistutorial@gmail.com
- jumlah commit dalam repository mempengaruhi nilai :D

## CONTOH STRUKTUR DALAM CLASS

```
<?php

class Categories {
    private $name;
    private $description;
    private $categories_model;

    public function __construct(CategoriesModel $categories_model)
    {
        $this->categories_model = $categories_model;
    }

    public function browse()
    {
        return $this->categories_model->browse();
    }

    public function show($id)
    {
        return $this->categories_model->show($id);
    }

    public function store($data = array())
    {
        return $this->categories_model->store($data);
    }

    public function update($id, $data = array())
    {
        return $this->categories_model->update($id, $data);
    }

    public function destroy($id)
    {
        return $this->categories_model->destroy($id);
    }
}

$category = new Categories;
echo $category->browse();
echo $category->show($id);
```

### SEMANGAT BERJUANG MENGERJAKAN UTSNYA, JANGAN LUPA BERDOA DULU

### SAYA YAKIN ANDA SEMUA PASTI BISA, :D

### TAK ADA USAHA YANG MEMBOHONGI HASIL ASALKAN KITA MAU BERUSAHA
