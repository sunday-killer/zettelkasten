202204060738
Tags: #компьютерные_сети

---

# Вставка битов (bit stuffing)
Вставка в начало и конец кадра специальной последовательности бит
- 01111110 - начало и конец кадра
- Если в данных встречается 6 или более идущих единиц, то в данные после каждых 5 последовательно идущих единиц добавляется 0. Получатель, после прочтения 5 последовательных 1 и встретил 0, этот 0 игнорирует

---
## Links