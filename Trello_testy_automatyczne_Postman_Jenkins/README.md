# ZINTEGROWANIE TESTÓW POSTMAN Z JENKINS
Uruchomiono przez użytkownika Agnieszka Mika
Running as SYSTEM
Building in workspace C:\ProgramData\Jenkins\.jenkins\workspace\Testy automatyczne Postman
[Testy automatyczne Postman] $ "C:\Program Files\Git\bin\sh.exe" -xe C:\WINDOWS\TEMP\jenkins11758980565566729034.sh
+ npm install -g newman
npm WARN deprecated har-validator@5.1.5: this library is no longer supported
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
npm WARN deprecated uuid@3.4.0: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.

added 111 packages, and audited 112 packages in 14s

5 packages are looking for funding
  run `npm fund` for details

found 0 vulnerabilities
+ newman run https://www.postman.com/collections/07c703ad06231f168662 -e 'https://api.getpostman.com/environments/21863765-11e68e06-3b2f-4660-953f-a841a9d0aa1d?apikey=PMAK-63313994dd455e5976129bf8-cff0d8a28ad63e316b9989dc6949f7b5f0'
newman

## KOLEKCJA Trello1

### Tablica Api
#### Stworzenie tablicy API
  POST https://api.trello.com/1/boards/?name=Tablica z API&key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 4kB, 586ms]
  √  Should verify status code
  √  Should verify board name
  √  Should verify response id lenght

#### Pokazywanie listy tablic
  GET https://api.trello.com/1/members/me/boards?key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 22.42kB, 246ms]
  √  Should verify status code
  √  Should verify type of board name

#### Tworzenie nowej listy w tablicy API
  POST https://api.trello.com/1/boards/633145777c28310194468541/lists?key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192&name=do korekty [200 OK, 2.36kB, 244ms]
  √  Should verify status code
  √  Should verify list name
  √  Should verify response id lenght

#### pokazywanie listy list tablicy API
  GET https://api.trello.com/1/boards/633145777c28310194468541/lists?key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 2.73kB, 180ms]
  √  Should verify response status
  √  Should verify closed value

#### aktualizacja listy w tablicy API
  PUT https://api.trello.com/1/lists/63314578a5cec3018ed8c6ff?name=Do poprawy&key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 2.35kB, 239ms]
  √  Should verify response status code
  √  Should verify updated name

#### dodanie nowej karty do listy w tablicy API
  POST https://api.trello.com/1/cards?idList=63314578a5cec3018ed8c6ff&key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192&name=Nie działa rejestracja [200 OK, 3.38kB, 382ms]
  √  Should verify status code
  √  Should verify id list and id board

#### lista kart w tablicy API
  GET https://api.trello.com/1/boards/633145777c28310194468541/cards?key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 3.27kB, 181ms]
  √  Should verify response status code
  √  Should verify id board and id list
  √  Should verify shortlink

#### aktualizacja karty w tablicy API
  PUT https://api.trello.com/1/cards/633145797fd6e8102be2f547?name=&key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192&desc= [200 OK, 3.29kB, 322ms]
  √  Should verify response status code
  √  Should verify updated description
  √  Should verify updated name

#### usunięcie karty z tablicy Api
  DELETE https://api.trello.com/1/cards/633145797fd6e8102be2f547?key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 2.24kB, 513ms]
  √  Should verify response status code

#### usunięcie stworzonej tablicy z API
  DELETE https://api.trello.com/1/boards/633145777c28310194468541?key=c40d5d8721be6b1550aaaa97482c94c2&token=499dfbb39b55649ef479e9a102eed83f2d1ed6161ae05b8d20e46e7c5d501192 [200 OK, 2.24kB, 596ms]
  √  Should verify status code

┌─────────────────────────┬─────────────────────┬────────────────────┐
│                         │            executed │             failed │
├─────────────────────────┼─────────────────────┼────────────────────┤
│              iterations │                   1 │                  0 │
├─────────────────────────┼─────────────────────┼────────────────────┤
│                requests │                  10 │                  0 │
├─────────────────────────┼─────────────────────┼────────────────────┤
│            test-scripts │                  20 │                  0 │
├─────────────────────────┼─────────────────────┼────────────────────┤
│      prerequest-scripts │                  10 │                  0 │
├─────────────────────────┼─────────────────────┼────────────────────┤
│              assertions │                  22 │                  0 │
├─────────────────────────┴─────────────────────┴────────────────────┤
│ total run duration: 4.5s                                           │
├────────────────────────────────────────────────────────────────────┤
│ total data received: 26.02kB (approx)                              │
├────────────────────────────────────────────────────────────────────┤
│ average response time: 348ms [min: 180ms, max: 596ms, s.d.: 153ms] │
└────────────────────────────────────────────────────────────────────┘
Finished: SUCCESS
