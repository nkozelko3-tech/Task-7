Тема 1. Числовые типы: int, double, num и математические операции
Задания для закрепления

<img width="1920" height="1038" alt="{8A0AB3AD-EA43-4347-812D-22CC18FD1840} png" src="https://github.com/user-attachments/assets/f8e9dcc7-1092-4ea0-beb3-a8d907eb5f49" />

1 Задание
void main() {
  int ru = 1000;
  double dollar = 81.13;

  String rawInput = "450.50";
  double? parsedPrice = double.tryParse(rawInput);

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

Тема 3. Логический тип (bool) и строгость условий
1 задание
<img width="1882" height="946" alt="3 тема 1 задание" src="https://github.com/user-attachments/assets/edd94beb-2c52-45e6-8c89-00001639c1b5" />

void main() {

  bool isAuthorized = true;
  bool isEmail = true;
  bool isBlocked = false;
  bool canAccess = isAuthorized && isEmail && !isBlocked;
}
2 задание
<img width="1898" height="966" alt="3 тема 2 задание " src="https://github.com/user-attachments/assets/c873cfdd-c9e4-4df3-8f16-6d8b6cd95ffa" />

  void main() {
 bool isBlank(String? input){
    return input == null || input.trim().isEmpty;
  }
}

3 задание
<img width="1907" height="972" alt="3 тема 3 задание" src="https://github.com/user-attachments/assets/82118ec0-d6f8-4d5f-80af-6c6c8e9dc3fe" />

  void main() {
bool isdark = false;
bool toggledark(bool isdark){
    return !isdark;
  }
}

4 задание
<img width="1915" height="970" alt="3 тема 4 задание" src="https://github.com/user-attachments/assets/21f33c22-2f0d-497d-b662-1fbf8a531c4e" />

  void main() {
int age = 33;
int drivingExpirience = 3;

bool canRentCar = age >= 21 && drivingExpirience >= 2;
}

5 задание
<img width="1911" height="970" alt="3 тема 5 задание" src="https://github.com/user-attachments/assets/73cefd1b-d0ff-4cdf-a8b0-6ba3b4a718d3" />

void main() {
  int userBalance = 100;
  bool isBalance = userBalance > 0;
  print(isBalance);
}

Тема 4. Списки (List): списковые включения и spread-операторы
<img width="1912" height="971" alt="image" src="https://github.com/user-attachments/assets/80ddef22-4eee-4128-9ef0-3aceb4bf3ce0" />

void main() {
  print('Задание 1: Удаление дубликатов');
  List<int> numbers = '1,1,2,2,3,4,4,5'.split(',').map(int.parse).toList();
  List<int> uniqueNumbers = numbers.toSet().toList();
  print('Исходный список: $numbers');
  print('Результат:       $uniqueNumbers\n');

  print('Задание 2: Пагинация среза');
  List<String> items = 'A,B,C,D,E,F,G,H'.split(',');
  print('Список элементов: $items');
  List<String> page = getPage(items, 2, 3); 
  print('Страница 2 (размер 3): $page\n');

  print('Задание 3: Сортировка по убыванию');
  List<double> prices = '10.5,45.0,5.2,100.0,23.9'.split(',').map(double.parse).toList();
  print('Цены до сортировки: $prices');
  prices.sort((a, b) => b.compareTo(a));
  print('Цены по убыванию:   $prices\n');

  print('Задание 4: Поиск слова > 8 символов');
  List<String> words = 'Dart,Flutter,Development,Code'.split(',');
  print('Список слов: $words');
  String longWord = words.firstWhere(
    (word) => word.length > 8,
    orElse: () => 'Ничего не найдено',
  );
  print('Первое длинное слово: $longWord\n');

  print('Задание 5: Генератор List.generate');
  List<String> slots = List.generate(10, (index) => 'Слот ${index + 1}');
  print('Сгенерированный список:');
  print(slots);
}

//Пагинация
List<T> getPage<T>(List<T> list, int page, int pageSize) {
  int startIndex = (page - 1) * pageSize;
  if (startIndex >= list.length || startIndex < 0) return [];
  
  int endIndex = startIndex + pageSize;
  if (endIndex > list.length) endIndex = list.length;
  
  return list.sublist(startIndex, endIndex);
}

Тема 5. Множества (Set) и Словари (Map): парсинг JSON-структур

<img width="1918" height="971" alt="image" src="https://github.com/user-attachments/assets/4dcf0f68-7655-48c8-8d12-8f729d4fb57f" />

void main() {
  print('Задание 1: Подсчет частоты слов');
  String text = 'dart flutter dart code flutter dart';
  Map<String, int> wordCounts = {};
  
  for (var word in text.split(' ')) {
    wordCounts[word] = (wordCounts[word] ?? 0) + 1;
  }
  print('Текст: "$text"');
  print('Результат частоты: $wordCounts\n');


  print('Задание 2: Симметрическая разность тегов');
  Set<String> setA = 'html,css,js'.split(',').toSet();
  Set<String> setB = 'js,node,git'.split(',').toSet();
  
  Set<String> uniqueTags = (setA.difference(setB)).union(setB.difference(setA));
  print('Множество A: $setA');
  print('Множество B: $setB');
  print('Результат разности: $uniqueTags\n');


  print('Задание 3: Безопасное извлечение настроек');
  Map<String, dynamic> settings = {
    'theme': 'dark',
    'fontSize': 14,
  };
  
  String getSetting(Map<String, dynamic> map, String key, String defaultValue) {
    var value = map[key];
    return (value is String) ? value : defaultValue;
  }
  
  print('Ищем существующий ключ "theme": ${getSetting(settings, "theme", "light")}');
  print('Ищем отсутствующий ключ "lang":  ${getSetting(settings, "lang", "ru")}\n');


  print('Задание 4: Трансформация карты (Курс доллара к рублю)');
  Map<String, double> rubPrices = {
    'Laptop': 80000.0,
    'Phone': 40000.0,
    'Book': 800.0,
  };
  double usdRate = 100.0;
  
  Map<String, double> usdPrices = rubPrices.map(
    (key, value) => MapEntry(key, double.parse((value / usdRate).toStringAsFixed(2))),
  );
  print('Цены в рублях:  $rubPrices');
  print('Цены в долларах: $usdPrices\n');


  print('Задание 5: Группировка пользователей по городу');
  List<Map<String, dynamic>> users = [
    {'name': 'Иван', 'city': 'Москва'},
    {'name': 'Анна', 'city': 'Питер'},
    {'name': 'Олег', 'city': 'Москва'},
  ];
  
  Map<String, List<Map<String, dynamic>>> groupedUsers = {};
  
  for (var user in users) {
    String city = user['city'] as String;
    groupedUsers.putIfAbsent(city, () => []).add(user);
  }
  
  print('Сгруппированный результат по городам:');
  groupedUsers.forEach((city, userList) {
    print('  $city: $userList');
  });
}

Тема 6. Null Safety, Records (кортежи) и Pattern Matching

1 задание


2 задание

<img width="1918" height="954" alt="image" src="https://github.com/user-attachments/assets/ea677636-fd15-4e93-8df9-ca031a2dcdec" />

void main() {
  String? bio; 
  String displayBio = bio ?? 'Информация отсутствует';
  print('Если bio null: "$displayBio"');
  
  bio = 'Flutter разработчик';
  displayBio = bio ?? 'Информация отсутствует';
  print('Если bio содержит текст: "$displayBio"');
}

3 задание

<img width="1903" height="957" alt="image" src="https://github.com/user-attachments/assets/151fe7eb-f650-4b55-bae9-ee5abf71df44" />

void main() {
String handleJson(Map<String, dynamic> json) {
  return switch (json) {
    {'id': var id} => 'Валидный объект с id = $id',
    {'error': var error} => 'Объект с полем ошибки: "$error"',
    _ => 'Неизвестный формат пакета'
  };
}

  Map<String, dynamic> response1 = {'id': 777, 'status': 'active'};
  Map<String, dynamic> response2 = {'error': 'Доступ запрещен'};

  print(handleJson(response1));
  print(handleJson(response2));
}

4 задание

<img width="1916" height="974" alt="image" src="https://github.com/user-attachments/assets/5de0c78f-d2e0-464c-9b30-9401ebffa176" />

void main() {
double runHeavyTask() {
  print('[Вычисление запущено!] Считаем сложные данные...');
  return 42.0 * 2.5;
}
  late final double expensiveCalculation = runHeavyTask();
  
  print('Шаг 1: Переменная объявлена. Вычислений еще не было.');
  
  print('Шаг 2: Первое обращение к переменной:');
  print('Значение = $expensiveCalculation');
  
  print('Шаг 3: Второе обращение к переменной (берется из кэша):');
  print('Значение = $expensiveCalculation');
}

5 задание

<img width="1869" height="951" alt="image" src="https://github.com/user-attachments/assets/230b1e79-7257-400a-a5a8-b093d8091974" />

void main() {
  List<int>? numbers;
  int firstElement = (numbers != null && numbers.isNotEmpty) ? numbers[0] : -1;
  print('Результат для null-списка: $firstElement'); 
  

  numbers = [];
  firstElement = (numbers != null && numbers.isNotEmpty) ? numbers[0] : -1;
  print('Результат для пустого списка: $firstElement');

}

50 Смешанных заданий по обработке данных
С 1 по 10 задания:
<img width="1480" height="748" alt="image" src="https://github.com/user-attachments/assets/b3308b5a-952c-4357-bb9c-82843d376316" />

void main() {
  double calculateTotalWithDiscount(double originalPrice) {
  double discount = originalPrice * 0.15;
  
  if (discount > 500) {
    discount = 500;
  }
  
  return originalPrice - discount;
}
}

<img width="1404" height="811" alt="image" src="https://github.com/user-attachments/assets/4afdae9b-70bb-4333-a049-7c43380f03fa" />

void main() {
String formatPrice(double price) {
  List<String> parts = price.toStringAsFixed(2).split('.');
  
  RegExp reg = RegExp(r'(\d{1,3})(?=(\d{3})+(?!\d))');
  String formattedInt = parts[0].replaceAllMapped(reg, (Match match) => '${match[1]} ');
  
  return '$formattedInt.${parts[1]} р.';
}
}

<img width="1429" height="594" alt="image" src="https://github.com/user-attachments/assets/53eb0777-c38e-483b-af07-3850b9dca21e" />

void main() {
int calculateCashback(int totalAmount) {
  return totalAmount ~/ 100;
}
}

<img width="1458" height="767" alt="image" src="https://github.com/user-attachments/assets/5aefbe7d-0b88-4b2c-b5eb-869d13330244" />

void main() {
double clampVolume(double volume) {
  return volume.clamp(0.0, 1.0);
}
}

<img width="1442" height="755" alt="image" src="https://github.com/user-attachments/assets/36e25a04-06a9-45bd-ad52-d9966ffbc1d9" />

void main() {
double bytesToMegabytes(int bytes) {
  double megabytes = bytes / (1024 * 1024);
  return double.parse(megabytes.toStringAsFixed(1));
}
}

<img width="1397" height="745" alt="image" src="https://github.com/user-attachments/assets/8969146c-2f87-434d-9332-044f045ea85b" />

void main() {
double calculateProgress(int current, int total) {
  if (total <= 0) return 0.0;
  return (current / total).clamp(0.0, 1.0);
}
}

<img width="1480" height="786" alt="image" src="https://github.com/user-attachments/assets/fa03c571-bc9b-422d-9d24-b4c6384e3bf9" />

void main() {
int roundToNextTen(int number) {
  return (number / 10).ceil() * 10;
}
}

<img width="1419" height="682" alt="image" src="https://github.com/user-attachments/assets/816cb88c-1ab9-4887-818b-d3054e08258d" />

void main() {
double calculateDeliveryCost(double distanceKm) {
  double baseCost = 200.0;
  if (distanceKm <= 5) {
    return baseCost;
  }
  return baseCost + (distanceKm - 5) * 30.0;
}
}

<img width="1360" height="729" alt="image" src="https://github.com/user-attachments/assets/7d78a5e8-73df-4f03-9959-7ac03c7b39a1" />

void main() {
bool isBlockDivisible(int packageSizeInBytes) {
  return packageSizeInBytes % 1024 == 0;
}
}

<img width="1357" height="780" alt="image" src="https://github.com/user-attachments/assets/7be74006-ff2a-4d33-ac72-67d4fface9c8" />

void main() {
Map<String, int> parsePriceRange(String priceText) {
  final regExp = RegExp(r'\d+');
  final matches = regExp.allMatches(priceText).map((m) => int.parse(m.group(0)!)).toList();

  return {
    'min': matches.isNotEmpty ? matches[0] : 0,
    'max': matches.length > 1 ? matches[1] : 0,
  };
}
}

С 11 по 20


<img width="1431" height="784" alt="image" src="https://github.com/user-attachments/assets/06b17f3b-7bc9-4e58-8902-b8cd8481c28a" />

void main() {
bool validatePassword(String password) {
  final regex = RegExp(r'^(?=.*[A-Z])(?=.*\d).{8,}$');
  return regex.hasMatch(password);
}
}

<img width="1399" height="705" alt="image" src="https://github.com/user-attachments/assets/362987c1-53a2-42ba-bf09-11b4405b38fa" />

void main() {
String cleanSearchInput(String input) {
  return input
      .toLowerCase()
      .replaceAll(RegExp(r'[#\$%]'), '')
      .replaceAll(RegExp(r'\s+'), ' ')  
      .trim();
}
}


<img width="1421" height="791" alt="image" src="https://github.com/user-attachments/assets/49d1eb36-1eb2-4a5d-ba02-67b746e01cfb" />

void main() {
String shortAuthorName(String fullName) {
  List<String> parts = fullName.trim().split(RegExp(r'\s+'));
  if (parts.length < 3) return fullName;
  return '${parts[0]} ${parts[1][0]}. ${parts[2][0]}.';
}
}


<img width="1425" height="768" alt="image" src="https://github.com/user-attachments/assets/da36b7a9-7271-4cfa-94c7-76bbd324b317" />

void main() {
int parseHexColor(String hexStr) {
  String cleanHex = hexStr.replaceAll('#', '');
  if (cleanHex.length == 6) {
    cleanHex = 'FF$cleanHex';
  }
  return int.parse(cleanHex, radix: 16);
}
}

<img width="1425" height="788" alt="image" src="https://github.com/user-attachments/assets/82a77b3f-b912-430f-adde-0e650e7bdaad" />

void main() {
String formatTimer(int seconds) {
  int minutes = seconds ~/ 60;
  int remainingSeconds = seconds % 60;
  
  String pad(int value) => value.toString().padLeft(2, '0');
  return '${pad(minutes)}:${pad(remainingSeconds)}';
}
}


<img width="1489" height="710" alt="image" src="https://github.com/user-attachments/assets/1a23a263-9d13-4600-9627-d050c87456f5" />

void main() {
String hidePhoneNumber(String phone) {

  if (phone.length != 12) return phone; 
  return '${phone.substring(0, 2)} (${phone.substring(2, 5)}) ***-**-${phone.substring(10)}';
}
}


<img width="1442" height="705" alt="image" src="https://github.com/user-attachments/assets/a695dbe4-7e1b-4923-8c72-a5a3e8ee7dd4" />

void main() {
bool hasCyrillic(String text) {
  for (int i = 0; i < text.length; i++) {
    int codeUnit = text.codeUnitAt(i);
    if ((codeUnit >= 0x0400 && codeUnit <= 0x04FF) || codeUnit == 0x0501) {
      return true;
    }
  }
  return false;
}
}


<img width="1430" height="744" alt="image" src="https://github.com/user-attachments/assets/1fbdcc39-4c07-413e-be7a-492e637c9721" />

void main() {
String slugify(String text) {
  final translit = {
    'а': 'a', 'б': 'b', 'в': 'v', 'г': 'g', 'д': 'd', 'е': 'e', 'ё': 'yo',
    'ж': 'zh', 'з': 'z', 'и': 'i', 'й': 'i', 'к': 'k', 'л': 'l', 'м': 'm',
    'н': 'n', 'о': 'o', 'п': 'p', 'р': 'r', 'с': 's', 'т': 't', 'у': 'u',
    'ф': 'f', 'х': 'kh', 'ц': 'ts', 'ч': 'ch', 'ш': 'sh', 'щ': 'shch',
    'ы': 'y', 'э': 'e', 'ю': 'yu', 'я': 'ya'
  };

  String result = text.toLowerCase();

  translit.forEach((cyr, lat) {
    result = result.replaceAll(cyr, lat);
  });

  return result
      .replaceAll(RegExp(r'[^a-z0-9\s-]'), '')
      .trim()
      .replaceAll(RegExp(r'\s+'), '-');
}
}


<img width="1387" height="769" alt="image" src="https://github.com/user-attachments/assets/a639b7c3-a1f0-4f6a-a983-c53b2a722b43" />

void main() {
int countWords(String text) {
  if (text.trim().isEmpty) return 0;
  return text.trim().split(RegExp(r'\s+')).length;
}
}


<img width="1407" height="752" alt="image" src="https://github.com/user-attachments/assets/ff3560b7-494c-4611-8d9a-4c975179e2cb" />

void main() {
List<String> extractHashtags(String text) {
  final regex = RegExp(r'#\w+');
  return regex.allMatches(text).map((match) => match.group(0)!).toList();
}
}

С 21 по 30

<img width="1473" height="810" alt="image" src="https://github.com/user-attachments/assets/3cdc861f-17f8-4881-9c32-233a4c3fbdba" />

void main() {
  print('=== ТЕСТИРОВАНИЕ БЛОКА 3: Списки, пагинация и фильтрация ===\n');


  final products = [
    Product(name: 'iPhone 15', price: 80000, rating: 4.8, category: 'Электроника', isAvailable: true),
    Product(name: 'Чехол для телефона', price: 500, rating: 4.1, category: 'Аксессуары', isAvailable: false),
    Product(name: 'MacBook Pro', price: 200000, rating: 4.9, category: 'Электроника', isAvailable: true),
    Product(name: 'Коврик для мыши', price: 1200, rating: 4.5, category: 'Аксессуары', isAvailable: true),
    Product(name: 'Книга по Dart', price: 2500, rating: 4.7, category: 'Книги', isAvailable: false),
  ];


  print('21. Фильтр цен (1000 - 50000):');
  final filteredByPrice = filterByPriceRange(products, 1000, 50000);
  for (var p in filteredByPrice) {
    print(' - ${p.name}: ${p.price} руб.');
  }


  print('\n22. Только активные задачи To-Do:');
  final todos = [
    TodoItem('Купить молоко', false),
    TodoItem('Сдать проект во Flutter', true),
    TodoItem('Помыть машину', false),
  ];
  final activeTodos = getActiveTodos(todos);
  for (var t in activeTodos) {
    print(' - ${t.task} (Выполнено: ${t.isCompleted})');
  }


  print('\n23. Инверсия порядка сообщений (in-place):');
  final chats = ['Привет!', 'Как дела?', 'Все отлично, пишу код на Dart', 'Супер!'];
  print(' До: $chats');
  reverseChatsInPlace(chats);
  print(' После: $chats');


  print('\n24. Объединение баннеров через spread (...):');
  final systemPromos = ['Баннер 1: Скидка 10%', 'Баннер 2: Черная Пятница'];
  final personalPromos = ['Баннер 3: Персональный промокод'];
  final allBanners = combineBanners(systemPromos, personalPromos);
  print(' Все баннеры: $allBanners');


  print('\n25. Товар с наивысшим рейтингом (.reduce):');
  final topRated = findTopRatedProduct(products);
  print(' - ${topRated.name} (Рейтинг: ${topRated.rating})');


  print('\n26. Вставка рекламы после каждого 5-го элемента ленты:');
  final newsFeed = List.generate(12, (index) => 'Новость №${index + 1}');
  final feedWithAds = insertAds(newsFeed, '=== РЕКЛАМНЫЙ БАННЕР ===');
  for (var item in feedWithAds) {
    print(' $item');
  }


  print('\n28. Уникальные категории товаров:');
  final uniqueCategories = getUniqueCategories(products);
  print(' Список: $uniqueCategories');


  print('\n29. Сортировка (Сначала в наличии, затем по возрастанию цены):');
  final sortedProducts = List<Product>.from(products);
  sortCatalog(sortedProducts);
  for (var p in sortedProducts) {
    print(' - В наличии: ${p.isAvailable.toString().padRight(5)} | Цена: ${p.price.toString().padRight(6)} | ${p.name}');
  }


  print('\n30. Разбиение 25 элементов на пачки по 10:');
  final longList = List.generate(25, (index) => 'Элемент $index');
  final chunks = chunkList(longList, 10);
  for (int i = 0; i < chunks.length; i++) {
    print(' Страница ${i + 1}: ${chunks[i]}');
  }
}



class Product {
  final String name;
  final double price;
  final double rating;
  final String category;
  final bool isAvailable;

  Product({
    required this.name,
    required this.price,
    required this.rating,
    required this.category,
    required this.isAvailable,
  });
}

class TodoItem {
  final String task;
  final bool isCompleted;

  TodoItem(this.task, this.isCompleted);
}



List<Product> filterByPriceRange(List<Product> items, double min, double max) {
  return items.where((item) => item.price >= min && item.price <= max).toList();
}


List<TodoItem> getActiveTodos(List<TodoItem> todos) {
  return todos.where((todo) => !todo.isCompleted).toList();
}


void reverseChatsInPlace(List<String> chatMessages) {
  int left = 0;
  int right = chatMessages.length - 1;
  while (left < right) {
    String temp = chatMessages[left];
    chatMessages[left] = chatMessages[right];
    chatMessages[right] = temp;
    left++;
    right--;
  }
}


List<String> combineBanners(List<String> promoBanners, List<String> personalBanners) {
  return [...promoBanners, ...personalBanners];
}


Product findTopRatedProduct(List<Product> products) {
  if (products.isEmpty) throw Exception("Список товаров пуст");
  return products.reduce((currentMax, product) => product.rating > currentMax.rating ? product : currentMax);
}

List<String> insertAds(List<String> news, String adBanner) {
  List<String> result = [];
  for (int i = 0; i < news.length; i++) {
    result.add(news[i]);
    if ((i + 1) % 5 == 0) {
      result.add(adBanner);
    }
  }
  return result;
}



List<String> getUniqueCategories(List<Product> products) {
  return products.map((p) => p.category).toSet().toList();
}


void sortCatalog(List<Product> products) {
  products.sort((a, b) {
    if (a.isAvailable != b.isAvailable) {
      return a.isAvailable ? -1 : 1; // Доступные товары перемещаются наверх
    }
    return a.price.compareTo(b.price); // При равной доступности — сортировка по цене
  });
}

List<List<T>> chunkList<T>(List<T> list, int chunkSize) {
  List<List<T>> chunks = [];
  for (int i = 0; i < list.length; i += chunkSize) {
    int end = (i + chunkSize < list.length) ? i + chunkSize : list.length;
    chunks.add(list.sublist(i, end));
  }
  return chunks;
}


С 31 по 40


<img width="1887" height="920" alt="image" src="https://github.com/user-attachments/assets/e916b5d4-f88c-4d93-b77f-65477143c57d" />

void main() {
  print('ТЕСТИРОВАНИЕ БЛОКА 4: Map, JSON-сериализация и кэширование\n');


  print('31. Десериализация профиля (с пустым/поврежденным JSON):');
  final Map<String, dynamic> brokenJson = {'id': null, 'name': null};
  final profile = UserProfile.fromJson(brokenJson);
  print(' - ID: ${profile.id}, Имя: ${profile.name}, Премиум: ${profile.isPremium}');


  print('\n32. Конвертация List<User> в Map<int, User>:');
  final usersList = [
    User(101, 'Алексей'),
    User(102, 'Мария'),
    User(103, 'Иван'),
  ];
  final usersMap = mapUsersById(usersList);
  usersMap.forEach((id, user) => print(' - Ключ (ID): $id -> Значение (Имя): ${user.name}'));


  print('\n33. Слияние профилей (Сервер в приоритете):');
  final localSettings = {'theme': 'dark', 'notifications': true, 'lang': 'ru'};
  final serverSettings = {'notifications': false, 'lang': 'en'};
  final mergedSettings = mergeProfiles(localSettings, serverSettings);
  print(' - Итоговые настройки: $mergedSettings');


  print('\n34. Очистка словаря от null перед отправкой:');
  final Map<String, dynamic> requestBody = {
    'title': 'Новый пост',
    'description': null,
    'views': 0,
    'authorId': null,
  };
  final cleanedBody = removeNullValues(requestBody);
  print(' - Исходный: $requestBody');
  print(' - Очищенный: $cleanedBody');


  print('\n35. Тестирование LRU-кэша страниц (лимит 5):');
  final cache = ScreenCache();
  cache.openScreen('Главная');
  cache.openScreen('Каталог');
  cache.openScreen('Корзина');
  cache.openScreen('Профиль');
  cache.openScreen('Настройки');
  print(' - Добавлено 5 страниц: ${cache.history}');
  cache.openScreen('Каталог');
  print(' - Открыли "Каталог" повторно (переместился в конец): ${cache.history}');
  cache.openScreen('Очередь_Заказов');
  print(' - Добавили 6-ю страницу (вытеснилась "Главная"): ${cache.history}');


  print('\n36. Инверсия словаря (Значения -> Ключи):');
  final codes = {'RU': 'Russia', 'US': 'USA', 'DE': 'Germany'};
  final invertedCodes = invertMap(codes);
  print(' - Исходный: $codes');
  print(' - Инвертированный: $invertedCodes');


  print('\n37. Общая сумма затрат по категориям товаров:');
  final cartItems = [
    {'name': 'Смартфон', 'category': 'Электроника', 'price': 60000.0},
    {'name': 'Наушники', 'category': 'Электроника', 'price': 15000.0},
    {'name': 'Футболка', 'category': 'Одежда', 'price': 2500.0},
    {'name': 'Книга', 'category': 'Книги', 'price': 1200.0},
    {'name': 'Джинсы', 'category': 'Одежда', 'price': 4500.0},
  ];
  final categoryTotals = calculateTotalByCategory(cartItems);
  categoryTotals.forEach((cat, total) => print(' - Категория: $cat -> Сумма: $total руб.'));


  print('\n38. Валидация JSON-ответа сервера:');
  final Map<String, dynamic> validResponse = {'status': 'success', 'data': [], 'timestamp': 1700000000};
  final Map<String, dynamic> invalidResponse = {'status': 'error', 'message': 'Not Found'};
  print(' - Ответ 1 валидный? ${validateJsonFields(validResponse)}');
  print(' - Ответ 2 валидный? ${validateJsonFields(invalidResponse)}');


  print('\n39. Группировка подкатегорий по parentId:');
  final flatCategories = [
    FlatCategory(1, null, 'Электроника'),
    FlatCategory(2, null, 'Одежда'),
    FlatCategory(3, 1, 'Смартфоны'),
    FlatCategory(4, 1, 'Ноутбуки'),
    FlatCategory(5, 2, 'Обувь'),
  ];
  final categoryTree = buildCategoryTree(flatCategories);
  categoryTree.forEach((parentId, list) {
    final parentName = parentId == null ? 'Корень' : 'ID родителя $parentId';
    final childrenNames = list.map((c) => c.name).toList();
    print(' - Уровень [$parentName]: $childrenNames');
  });


  print('\n40. Сериализация фильтров в query-строку URL:');
  final filters = {'brand': 'Apple', 'minPrice': 50000, 'search query': 'pro max'};
  final urlQuery = serializeFilterToUrl(filters);
  print(' - Строка параметров: $urlQuery');
}



class User {
  final int id;
  final String name;
  User(this.id, this.name);
}

class FlatCategory {
  final int id;
  final int? parentId;
  final String name;
  FlatCategory(this.id, this.parentId, this.name);
}


class UserProfile {
  final int id;
  final String name;
  final bool isPremium;

  UserProfile.fromJson(Map<String, dynamic> json)
      : id = json['id'] as int? ?? 0,
        name = json['name'] as String? ?? "Гость",
        isPremium = json['isPremium'] as bool? ?? false;
}


Map<int, User> mapUsersById(List<User> users) {
  return { for (var user in users) user.id : user };
}


Map<String, dynamic> mergeProfiles(Map<String, dynamic> localCache, Map<String, dynamic> serverData) {
  return {...localCache, ...serverData};
}


Map<String, dynamic> removeNullValues(Map<String, dynamic> jsonMap) {
  return Map<String, dynamic>.from(jsonMap)..removeWhere((key, value) => value == null);
}


class ScreenCache {
  final List<String> _cache = [];

  void openScreen(String screenName) {
    _cache.remove(screenName); 
    _cache.add(screenName);   
    
    if (_cache.length > 5) {
      _cache.removeAt(0);      
    }
  }

  List<String> get history => List.unmodifiable(_cache);
}


Map<String, String> invertMap(Map<String, String> original) {
  return original.map((key, value) => MapEntry(value, key));
}


Map<String, double> calculateTotalByCategory(List<Map<String, dynamic>> items) {
  final Map<String, double> totals = {};
  for (var item in items) {
    final String category = item['category'] as String? ?? 'Разное';
    final double price = (item['price'] as num? ?? 0.0).toDouble();
    totals[category] = (totals[category] ?? 0.0) + price;
  }
  return totals;
}


bool validateJsonFields(Map<String, dynamic> json) {
  final requiredKeys = {'status', 'data', 'timestamp'};
  return requiredKeys.every((key) => json.containsKey(key));
}


Map<int?, List<FlatCategory>> buildCategoryTree(List<FlatCategory> categories) {
  final Map<int?, List<FlatCategory>> tree = {};
  for (var cat in categories) {
    tree.putIfAbsent(cat.parentId, () => []).add(cat);
  }
  return tree;
}


String serializeFilterToUrl(Map<String, dynamic> filters) {
  return filters.entries
      .map((e) => '${Uri.encodeComponent(e.key)}=${Uri.encodeComponent(e.value.toString())}')
      .join('&');
}

С 41 по 50 НАКОНЕЦ-ТО УРААА


<img width="1453" height="851" alt="image" src="https://github.com/user-attachments/assets/a6e32c34-df84-40d7-80a6-6080db02b1a9" />

void main() {
  print('ТЕСТИРОВАНИЕ БЛОКА 5: Sound Null Safety, Records и пайплайны\n');


  print('41. Парсер геолокации через Record:');
  final coords = parseGeolocation("54.01, 38.29");
  if (coords != null) {
    print(' - Широта (lat): ${coords.$1}, Долгота (lon): ${coords.$2}');
  }


  print('\n42. Резолвер состояний загрузки:');
  print(' - State 1: ${getStatusMessage((isLoading: true, hasError: false))}');
  print(' - State 2: ${getStatusMessage((isLoading: false, hasError: true))}');
  print(' - State 3: ${getStatusMessage((isLoading: false, hasError: false))}');


  print('\n43. Безопасная цепочка вызовов deep null:');
  final sampleUser = User(Company(Address('улица Пушкина')));
  User? nullUser;
  print(' - С данными: ${getUserStreet(sampleUser)}');
  print(' - Null-объект: ${getUserStreet(nullUser)}');



  print('\n45. Деструктуризация точек в цикле for:');
  final pointList = [(10, 20), (35, 45), (100, 200)];
  processPoints(pointList);


  print('\n46. Обмен значений через кортежи:');
  int a = 5;
  int b = 10;
  print(' - До: a = $a, b = $b');
  (a, b) = (b, a);
  print(' - После: a = $a, b = $b');


  print('\n47. Валидатор формы регистрации:');
  final formResult = validateRegistrationForm("user@example.com", "123", "123");
  print(' - Форма валидна? ${formResult.isValid}');
  print(' - Ошибки: ${formResult.errors}');


  print('\n48. Обработка диапазона громкости через conditions (when):');
  print(' - Громкость 90: ${getVolumeStatus(90)}');
  print(' - Громкость 5: ${getVolumeStatus(5)}');
  print(' - Громкость 50: ${getVolumeStatus(50)}');


  print('\n49. Пайплайн очистки телефонной книги:');
  final dirtyNumbers = ['+7 (999) 123-45-67', null, '   ', '8-999-123-45-67', '+7(999)1234567'];
  final cleanBook = cleanPhoneBook(dirtyNumbers);
  print(' - Исходный: $dirtyNumbers');
  print(' - Уникальные очищенные номера: $cleanBook');


  print('\n50. Аналитический модуль корзины:');
  final shoppingCart = [
    {'name': 'Кроссовки', 'category': 'Обувь', 'price': 5000.0, 'count': 1, 'discount': 10.0}, // 5000 - 10% = 4500
    {'name': 'Носки', 'category': 'Одежда', 'price': 300.0, 'count': 3, 'discount': 0.0},     // 900
    {'name': 'Шоколадка', 'category': 'Еда', 'price': 150.0, 'count': 2, 'discount': 20.0},   // 300 - 20% = 240
  ];
  final analytics = analyzeCart(shoppingCart);
  print(' - Итого к оплате (total): ${analytics.total} руб.');
  print(' - Сэкономлено (discountAmount): ${analytics.discountAmount} руб.');
  print(' - Бесплатная доставка? ${analytics.isFreeDelivery}');
}



class User {
  final Company? company;
  User(this.company);
}

class Company {
  final Address? address;
  Company(this.address);
}

class Address {
  final String? street;
  Address(this.street);
}




(double lat, double lon)? parseGeolocation(String coordsStr) {
  final parts = coordsStr.split(',');
  if (parts.length != 2) return null;

  final lat = double.tryParse(parts[0].trim());
  final lon = double.tryParse(parts[1].trim());

  if (lat == null || lon == null) return null;
  return (lat, lon);
}


String getStatusMessage(({bool isLoading, bool hasError}) state) {
  return switch (state) {
    (isLoading: true, hasError: _) => "Идет загрузка данных...",
    (isLoading: false, hasError: true) => "Произошла ошибка при загрузке.",
    (isLoading: false, hasError: false) => "Данные успешно отображены."
  };
}


String getUserStreet(User? user) {
  return user?.company?.address?.street ?? "Адрес не указан";
}




void processPoints(List<(int x, int y)> points) {
  for (var (x, y) in points) {
    print(' - Извлечена точка -> X: $x, Y: $y');
  }
}




({bool isValid, List<String> errors}) validateRegistrationForm(String email, String password, String confirmPassword) {
  final List<String> errors = [];
  
  if (!email.contains('@')) errors.add("Неверный формат Email");
  if (password.length < 6) errors.add("Пароль должен быть не менее 6 символов");
  if (password != confirmPassword) errors.add("Пароли не совпадают");

  return (isValid: errors.isEmpty, errors: errors);
}


String getVolumeStatus(int volume) {
  return switch (volume) {
    int v when v > 80 => "Слишком громко!",
    int v when v < 10 => "Слишком тихо!",
    _ => "Оптимальная громкость"
  };
}


Set<String> cleanPhoneBook(List<String?> dirtyPhones) {
  return dirtyPhones
      .whereType<String>() // Избавляемся от null значений
      .map((phone) => phone.replaceAll(RegExp(r'\D'), '')) // Удаляем всё, кроме цифр
      .where((phone) => phone.isNotEmpty) // Отсекаем пустые строки
      .toSet(); // Оставляем только уникальные значения
}


({double total, double discountAmount, bool isFreeDelivery}) analyzeCart(List<Map<String, dynamic>> cart) {
  double totalWithoutDiscount = 0.0;
  double finalTotal = 0.0;

  for (var item in cart) {
    final double price = (item['price'] as num? ?? 0.0).toDouble();
    final int count = (item['count'] as int? ?? 1);
    final double discountPercent = (item['discount'] as num? ?? 0.0).toDouble();

    final double originalCost = price * count;
    totalWithoutDiscount += originalCost;

    final double discountAmountForPosition = originalCost * (discountPercent / 100.0);
    finalTotal += (originalCost - discountAmountForPosition);
  }

  final double totalDiscountAmount = totalWithoutDiscount - finalTotal;
  final bool isFreeDelivery = finalTotal >= 2000.0;

  return (
    total: finalTotal,
    discountAmount: totalDiscountAmount,
    isFreeDelivery: isFreeDelivery
  );
}

отдельно 44 

<img width="1440" height="729" alt="image" src="https://github.com/user-attachments/assets/7ad278a8-6b72-486a-ad3e-32ded88197ef" />

void main() {

  final dynamic responseSuccessCode = 200;
  final dynamic responseServerStringError = "Internal Server Error (500)";
  final dynamic responseJsonData = {
    'id': 777,
    'title': 'Изучаем Flutter и Dart в 2026 году',
    'status': 'published'
  };
  final dynamic responseUnknownType = 45.67; 


  print(handleApiResponse(responseSuccessCode));
  print(handleApiResponse(responseServerStringError));
  print(handleApiResponse(responseJsonData));
  print(handleApiResponse(responseUnknownType));
}


String handleApiResponse(dynamic response) {
  return switch (response) {
    int code => "Код ответа сервера (int): $code",
    String error => "Текстовая ошибка (String): $error",
    Map data => "Успешно получена карта данных (Map). Количество ключей: ${data.length}",
    _ => "Ошибка: Неизвестный или неподдерживаемый тип ответа API"
  };
}

