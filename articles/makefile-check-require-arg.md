---
title: "Makefileの引数が定義されてるか確認する方法メモ"
emoji: "🐰"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["make", "makefile"]
published: false
---

Makefileで引数が確認されてるか確認する方法として擬似ターゲット（`.PHONY`）と`ifdef`を組み合わせる方法がよく紹介されている。



makeをタスクランナーとして使う場合はこれでも良いが、ビルドツールとして使うときは依存ターゲットに擬似ターゲットが含まれていると毎回ビルドを実行することになるのでとても不便である。（特にビルド時間が長いときは顕著）
