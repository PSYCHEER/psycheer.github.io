---
title: 'Jak přispět'
description: 'Průvodce, jak přispět do wiki'
hide:
    - footer
icon: material/github
---

# Jak přispět do GitHubu

Přispívání do našeho GitHub repozitáře je skvělý způsob, jak pomoci zlepšit projekt. Postupujte podle těchto kroků:

## 1. Forkněte Repozitář

Nejprve musíte forkout repozitář. Tím vytvoříte kopii repozitáře pod vaším vlastním GitHub účtem.

1. Přejděte na repozitář: [PSYCHEER/psycheer.github.io](https://github.com/PSYCHEER/psycheer.github.io)
2. Klikněte na tlačítko "Fork" v pravém horním rohu stránky.

## 2. Naklonujte Forknutý Repozitář

Dále naklonujte forknutý repozitář do vašeho lokálního počítače.

```sh
git clone https://github.com/PSYCHEER/psycheer.github.io.git
cd psycheer.github.io
```

## 3. Vytvořte Novou Větev

Vytvořte novou větev, na které budete pracovat na svých změnách.

```sh
git checkout -b moje-nova-vetv
```

Nahraďte `moje-nova-vetv` popisným názvem pro vaši větev.

## 4. Upravte Soubory

Proveďte potřebné změny v souborech. Můžete použít jakýkoli textový editor nebo IDE k úpravě souborů.
??? tip
    Naše doporučení je [VS-Code](https://code.visualstudio.com)

## 5. Commitněte Vaše Změny

Po provedení změn je commitněte do vaší větve.

```sh
git add .
git commit -m "Popis změn"
```

## 6. Pushněte Vaše Změny

Pushněte vaše změny do vašeho forknutého repozitáře na GitHubu.

```sh
git push origin moje-nova-vetv
```

## 7. Vytvořte Pull Request

Nakonec vytvořte pull request, aby se vaše změny mohly sloučit do původního repozitáře.

1. Přejděte na váš forknutý repozitář na GitHubu.
2. Klikněte na tlačítko "Compare & pull request".
3. Poskytněte název a popis pro váš pull request.
4. Klikněte na tlačítko "Create pull request".

Váš pull request bude zkontrolován a pokud bude vše v pořádku, bude sloučen do hlavního repozitáře.

Děkujeme za váš příspěvek! 💖👑