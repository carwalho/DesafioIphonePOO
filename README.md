# 📱 Desafio POO - iPhone (Java)

Este projeto foi desenvolvido como parte de um desafio de Programação Orientada a Objetos (POO) proposto na DIO. O objetivo é simular, em Java, o funcionamento de um iPhone com três principais funcionalidades:

- 🎵 Reprodutor Musical
- 📞 Aparelho Telefônico
- 🌐 Navegador de Internet

---

## 🧠 Conceitos aplicados

- Interfaces em Java
- Implementação de múltiplas interfaces
- Encapsulamento
- Organização em pacotes/classes
- Diagrama UML com Mermaid

---

## 🖼️ Diagrama UML (Mermaid)

```mermaid
classDiagram
    class ReprodutorMusical {
        +tocar()
        +pausar()
        +selecionarMusica(String musica)
    }

    class AparelhoTelefonico {
        +ligar(String numero)
        +atender()
        +iniciarCorreioVoz()
    }

    class NavegadorInternet {
        +exibirPagina(String url)
        +adicionarNovaAba()
        +atualizarPagina()
    }

    interface Reprodutor {
        +tocar()
        +pausar()
        +selecionarMusica(String musica)
    }

    interface Telefone {
        +ligar(String numero)
        +atender()
        +iniciarCorreioVoz()
    }

    interface Navegador {
        +exibirPagina(String url)
        +adicionarNovaAba()
        +atualizarPagina()
    }

    class iPhone

    iPhone ..|> Reprodutor
    iPhone ..|> Telefone
    iPhone ..|> Navegador

    Reprodutor <|.. ReprodutorMusical
    Telefone <|.. AparelhoTelefonico
    Navegador <|.. NavegadorInternet
