Тема 1. Числовые типы: int, double, num и математические операции
Задания для закрепления

<img width="1920" height="1038" alt="{8A0AB3AD-EA43-4347-812D-22CC18FD1840} png" src="https://github.com/user-attachments/assets/f8e9dcc7-1092-4ea0-beb3-a8d907eb5f49" />

1 Задание
void main() {
  int ru = 1000;
  double dollar = 81.13;

  // Безопасный парсинг строк
  String rawInput = "450.50";
  double? parsedPrice = double.tryParse(rawInput);

  // Округление и форматирование
  double itemPrice = ru * dollar;
  print("До 2 знаков: ${itemPrice.toStringAsFixed(2)}"); // "129.90"
}

<img width="1918" height="1080" alt="1тема задание 2" src="https://github.com/user-attachments/assets/48ca3e5b-d41c-4a06-87a0-61c1a74ac40f" />

2 Задание 
void main(){
int Age(String input){
   return int.tryParse(input) ?? -1; 
}
print (Age("25"));
print (Age("abc"));
}

<img width="1920" height="1080" alt="1тема задание 3" src="https://github.com/user-attachments/assets/405bb768-60cd-44c8-9982-d2d2ec34ebfa" />

3 Задание
void main(){

double plotnoct (int px, double density){
    return px / density;
}
int plotnost (int px, int density){
    return px ~/ density;
}
}

<img width="1920" height="1080" alt="1 тема задание 4" src="https://github.com/user-attachments/assets/bf95232f-60b5-4c06-bed8-1bc9ea49db8d" />

4 Задание
void main(){
  int sensor (bool sensorA, sensorB, sensorC){
    int kod = 0;

    if (sensorA) kod |=(1<<0);
    if (sensorB) kod |=(1<<1);
    if (sensorC) kod |=(1<<2);

    return kod;
  }
  int state = sensor(true, false, true);
  print(state.toRadixString(2));
}

<img width="1920" height="1080" alt="1 тема задание 5" src="https://github.com/user-attachments/assets/ca52b25f-b8a0-4a9a-b429-963a64cb637c" />

5 Задание
void main(){
  bool raw (int number){
    return (number & 1) == 0;
  }
  print (raw(7));
  print (raw(36));
}

Тема 2. Строки (String), интерполяция и кодовые точки (Runes)

<img width="1920" height="1080" alt="2 тема 1 задание" src="https://github.com/user-attachments/assets/b2850d03-37fe-4a8f-9d84-8efc85fb8f95" />

1 Задание 
void main() {
 String maskEmail(String email) {
  List<String> parts = email.split('@');
  if (parts.length != 2) return email; 

  String localPart = parts[0];
  String domain = parts[1];

  if (localPart.length <= 2) {
    return localPart.replaceAll(RegExp(r'.'), '*') + '@' + domain;
  }

  String firstChar = localPart[0];
  String lastChar = localPart[localPart.length - 1];
  String stars = '*' * (localPart.length - 2);

  return '$firstChar$stars$lastChar@$domain';
}
  print(maskEmail("ivanov.flutter@gmail.com")); 
}

<img width="1920" height="1080" alt="2 тема 2 задание" src="https://github.com/user-attachments/assets/f8618b65-f493-4501-9419-75e769c3553d" />

2 Задание
void main() {
 bool silka(String max){
  return max.startsWith('https://');
 }
 print(silka('htps://porhub.com'));
 print(silka('https://maxgovno.ru'));
}

<img width="1920" height="1080" alt="2 ТЕМА ЗАДАНИЕ 3" src="https://github.com/user-attachments/assets/526200b9-99f6-401f-a8a8-dcf120b0e624" />

3 Задание
void main() {
String getMonogram(String fullName) {
  return fullName
      .split(' ')                          
      .where((word) => word.isNotEmpty)    
      .map((word) => word[0].toUpperCase()) 
      .join('');                           
}

  print(getMonogram('Душаков Иван Лерикович Добрав Омлет')); 
}

<img width="1920" height="1080" alt="2 тема задание 4" src="https://github.com/user-attachments/assets/722a742d-c7b8-4c9f-8b97-42bcf380c75b" />

4 задание 
void main() {
void parseCartItem(String csvRow) {
  
  List<String> parts = csvRow.split(',');

  String name = parts[0];
  int quantity = int.parse(parts[1]);
  double price = double.parse(parts[2]);

  print('Наименование: $name');
  print('Количество: $quantity');
  print('Стоимость: $price');
}
  parseCartItem("яблоко,3,150.5");
}

<img width="1920" height="1080" alt="2 тема 5 задание" src="https://github.com/user-attachments/assets/5d4876e6-3000-4960-b09c-f3a0049b9750" />

5 задание 
void main() {
int getRealLength(String text) {
  return text.runes.length;
}


  String statusMessage = "Статус заказа: Доставлен 🚀";
  
  print("Обычная длина (.length): ${statusMessage.length}"); 
  print("Реальная длина (.runes.length): ${getRealLength(statusMessage)}");
}
