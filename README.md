<h1>Домашнее задание по теме 13. Строка как массив символов</>

<h2>Задача - Написать программу, удаляющую первую букву каждого слова.</h2>

<h2>Блок-схема:</h2>
<h3>Функция main()</h3>
<img width="350" height="900" alt="main()" src="https://github.com/user-attachments/assets/a6078a0b-7e84-44b5-880d-540bf64cfd15" />

<h2>Код:</h2>

```c
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h>

int main() {

	char buf[100];
	int len;

	fgets(buf, sizeof(buf), stdin);

	len = strlen(buf);

	if (buf[0] != ' ') {
		buf[0] = ' ';
	}

	for (int i = 1; i < len; i++) {
		if (buf[i] == ' ' && i != len - 1 && buf[i - 1] != ' ') {
			buf[i + 1] = ' ';
		}
	}

	printf("\n%s", buf);

	return 0;
}
```
