---
title: 'Jak współtworzyć'
description: 'Przewodnik, jak współtworzyć wiki'
hide:
    - footer
icon: material/github
---

# Jak współtworzyć na GitHub

Współtworzenie naszego repozytorium GitHub to świetny sposób na ulepszenie projektu. Postępuj zgodnie z tymi krokami, aby współtworzyć:

## 1. Sforkuj repozytorium

Najpierw musisz sforkować repozytorium. Tworzy to kopię repozytorium na Twoim koncie GitHub.

1. Przejdź do repozytorium: [PSYCHEER/psycheer.github.io](https://github.com/PSYCHEER/psycheer.github.io)
2. Kliknij przycisk "Fork" w prawym górnym rogu strony.

## 2. Sklonuj sforkowane repozytorium

Następnie sklonuj sforkowane repozytorium na swój lokalny komputer.

```sh
git clone https://github.com/PSYCHEER/psycheer.github.io.git
cd psycheer.github.io
```

## 3. Utwórz nową gałąź

Utwórz nową gałąź (branch), aby pracować nad swoimi zmianami.
```sh
git checkout -b my-new-branch
```

Zastąp my-new-branch opisową nazwą dla swojej gałęzi.

## 4. Edytuj pliki

Wprowadź niezbędne zmiany w plikach. Możesz użyć dowolnego edytora tekstu lub IDE.
??? tip
    Nasza rekomendacja to [VS-Code](https://code.visualstudio.com)

## 5. Zatwierdź swoje zmiany

Po wprowadzeniu zmian zatwierdź je w swojej gałęzi.

```sh
git add .
git commit -m "Opis wprowadzonych zmian"
```

## 6. Wypchnij swoje zmiany

Wypchnij swoje zmiany do sforkowanego repozytorium na GitHub.

```sh
git push origin my-new-branch
```

## 7. Utwórz Pull Request

Na koniec utwórz pull request, aby wprowadzić swoje zmiany do oryginalnego repozytorium.

1. Przejdź do swojego sforkowanego repozytorium na GitHub.
2. Kliknij przycisk "Compare & pull request".
3. Podaj tytuł i opis swojego pull requesta.
4. Kliknij przycisk "Create pull request".

Twój pull request zostanie przejrzany, a jeśli wszystko będzie w porządku, zostanie scalony z głównym repozytorium.

Dziękujemy za współtworzenie! 💖👑