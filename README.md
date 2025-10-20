# 📅 App Agenda

Aplicativo Android simples desenvolvido em **Java + XML** no **Android Studio**, que permite ao usuário adicionar compromissos à sua agenda e visualizá-los em uma lista.  
Projeto criado como parte dos estudos de **desenvolvimento mobile nativo** e para praticar manipulação de listas e interações com o usuário.

---

## 🧠 Sobre o Projeto

O **App Agenda** oferece uma interface onde o usuário pode inserir detalhes de compromissos, como título, data e descrição, e ao clicar em um botão, esses dados são adicionados a uma lista exibida na tela.  
O objetivo é demonstrar como coletar entradas do usuário e exibir os dados dinamicamente em uma lista.

---

## 🛠️ Tecnologias Utilizadas

| Categoria         | Ferramenta                         |
|-------------------|------------------------------------|
| IDE               | Android Studio                     |
| Linguagem         | Java                               |
| Layouts           | XML                                |
| Versão mínima Android | API 21 (Android 5.0)             |
| Estrutura de UI   | ConstraintLayout / LinearLayout    |

---

## 📱 Estrutura do Projeto

```
app/
 ├── java/
 │    └── br/ulbra/appagenda/
 │         └── MainActivity.java
 ├── res/
 │    ├── layout/
 │    │     └── activity_main.xml
 │    ├── drawable/
 │    │     └── (ícones ou imagens do app)
 │    └── values/
 │          └── strings.xml
 └── AndroidManifest.xml
```

---

## 🧩 Lógica de Adição de Compromissos

```java
EditText edtTitulo = findViewById(R.id.edtTitulo);
EditText edtData = findViewById(R.id.edtData);
EditText edtDescricao = findViewById(R.id.edtDescricao);
Button btnAdicionar = findViewById(R.id.btnAdicionar);
ListView listView = findViewById(R.id.listView);

btnAdicionar.setOnClickListener(v -> {
    String titulo = edtTitulo.getText().toString();
    String data = edtData.getText().toString();
    String descricao = edtDescricao.getText().toString();
    if (!titulo.isEmpty() && !data.isEmpty() && !descricao.isEmpty()) {
        String compromisso = "Título: " + titulo + "\nData: " + data + "\nDescrição: " + descricao;
        listaCompromissos.add(compromisso);
        adapter.notifyDataSetChanged();
        edtTitulo.setText("");
        edtData.setText("");
        edtDescricao.setText("");
    }
});
```

---

## 🏗️ Funcionalidades Implementadas

✅ Adicionar compromissos à agenda  
✅ Exibir lista de compromissos na tela  
✅ Interface simples e funcional  
✅ Código comentado para entendimento  

---

## 💡 Possíveis Melhorias

- Implementar funcionalidade para editar ou remover compromissos  
- Adicionar persistência de dados utilizando banco de dados local (SQLite)  
- Implementar ordenação dos compromissos por data  
- Adicionar notificações para lembrar o usuário dos compromissos  
- Implementar busca por título ou data dos compromissos  

---

## 👩‍💻 Autor

**Nome:** *Laerte Ferraz da Silva Júnior*  
**Instituição:** *Curso Técnico em Informática – Escola Ulbra São Lucas*  
**Disciplina:** *Desenvolvimento Mobile Android*  
**Professor:** *Jeferson Leon*  

---

## 📚 Licença

Projeto desenvolvido para fins **educacionais**.  
Livre para uso e modificação, desde que mantidos os créditos ao autor.

---

> “A melhor forma de aprender é construindo. Então... bora codar!”
