 # OOP pada Dart #

List

Daftar hanyalah sekelompok objek yang dipesan. Pustaka dart: core menyediakan kelas Daftar yang memungkinkan pembuatan dan manipulasi daftar.

Daftar menggunakan pengindeksan berbasis nol, di mana 0 adalah indeks dari elemen pertama dan list.length - 1 adalah indeks dari elemen terakhir. Anda bisa mendapatkan panjang daftar dan merujuk ke elemen daftar seperti yang Anda lakukan di JavaScript:

Syntax
var list = [1, 2, 3];

var list_name = new List(initial_size)

example

void main() { 
   var lst = new List(3); 
   lst[0] = 12; 
   lst[1] = 13; 
   lst[2] = 11; 
   print(lst); 
}


Map

Objek Peta adalah pasangan kunci / nilai sederhana. Kunci dan nilai dalam peta dapat berupa jenis apa pun. Peta adalah koleksi dinamis. Dengan kata lain, Peta dapat tumbuh dan menyusut pada saat runtime

Pada umumnya, peta adalah objek yang mengaitkan kunci dan nilai. Baik kunci dan nilai dapat berupa jenis objek apa pun. Setiap tombol hanya terjadi sekali, tetapi Anda dapat menggunakan nilai yang sama beberapa kali. Dukungan dart untuk peta disediakan oleh literal peta dan tipe Peta.

Syntax
var identifier = { key1:value1, key2:value2 [,…..,key_n:value_n] }

example

void main() { 
   var details = {'Usrname':'tom','Password':'pass@123'}; 
   print(details); 
}


Set

Set mewakili kumpulan objek di mana setiap objek hanya dapat terjadi sekali. Pustaka dart: core menyediakan kelas Set untuk mengimplementasikan hal yang sama.

Syntax:
Identifier = new Set()
Example
void main() { 
   Set numberSet = new  Set(); 
   numberSet.add(100); 
   numberSet.add(20); 
   numberSet.add(5); 
   numberSet.add(60); 
   numberSet.add(70);
   print("Default implementation :${numberSet.runtimeType}");  
   
   for(var no in numberSet) { 
      print(no); 
   } 
}    
Collection
Perpustakaan dart: collection menyediakan kelas yang memungkinkan berbagai implementasi koleksi Dart. 

1.	Hashmap

HashMap adalah implementasi peta berbasis hash table. Saat Anda melakukan iterasi melalui kunci atau nilai HashMap, Anda tidak bisa mengharapkan pesanan tertentu. 
Syntax
Identifier= new HashMap()
Example
import 'dart:collection'; 
main() { 
   var accounts = new HashMap(); 
   accounts['dept']='HR'; 
   accounts['name']='Tom'; 
   accounts['email']='tom@xyz.com'; 
   print('Map after adding  entries :${accounts}'); 
}


2.	Hashset

HashSet adalah implementasi Set berbasis tabel hash yang tidak teratur\

Syntax
Identifier = new HashSet() 
Fungsi add () dapat digunakan untuk mengisi instance HashSet.

Example
Live Demo
import 'dart:collection'; 
void main() { 
   Set numberSet = new  HashSet(); 
   numberSet.add(100); 
   numberSet.add(20); 
   numberSet.add(5); 
   numberSet.add(60); 
   numberSet.add(70); 
   print("Default implementation :${numberSet.runtimeType}"); 
   for(var no in numberSet){ 
      print(no); 
   }


Generic 
Deklarasi generik menginduksi keluarga deklarasi, satu untuk setiap set parameter tipe aktual yang disediakan dalam program.


Generic string collection
Collection<String> list = ['a','b','c'];

Generic Integer List
List<int> list = [11,12,13];

Generics String List
List<String> list = new List<String>();

Generics String List
var list = new List<String>();

Generics with HashSet
HashSet<String> collection = new HashSet<String>();

Generics with HashSet
var collection = new HashSet<String>();

Generics with Map and HashMap
Map<String, double> map = new HashMap<String, double>();

Generics with Map and HashMap
var map = new HashMap<String, double>();


example
class Location<E> {
  E lat, lng;
  
  Location(this.lat, this.lng);
  
  toString() => "Have you been to ${lat}, ${lng}?";
}

void main() {
  var location1 = new Location<double>(21.271488, -157.822806);
  print(location1);
  
  var location2 = new Location<String>('21.271488', '-157.822806');
  print(location2);
  
  var location3 = new Location<int>(21, -157);
  print(location3);
}

