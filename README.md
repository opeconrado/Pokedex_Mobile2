# Pokédex com Firebase e API Pokémon

## 🌟 Visão Geral

A Pokédex é uma aplicação Flutter que permite aos usuários:
- Criar contas e fazer login usando Firebase Authentication
- Explorar uma lista completa de Pokémon
- Visualizar detalhes como tipos, habilidades, peso e altura
- Buscar Pokémon por nome

## ✨ Funcionalidades

### Autenticação
- Cadastro de novos usuários
- Login com e-mail e senha
- Validação de formulários
- Feedback visual com SnackBar

### Pokédex
- Listagem de 150 Pokémon
- Busca em tempo real
- Cards coloridos por tipo
- Detalhes completos de cada Pokémon
- Imagens animadas (sprites)

## 🛠 Tecnologias

**Principais tecnologias utilizadas:**
- **Flutter** 3.0+ - Framework para desenvolvimento multiplataforma
- **Firebase Auth** - Autenticação de usuários
- **PokéAPI** - API pública com dados de Pokémon
- **HTTP** - Para requisições à API
- **Google Fonts** - Tipografia personalizada

**Dependências principais:**
```yaml
dependencies:
  flutter:
    sdk: flutter
  firebase_core: ^2.15.0
  firebase_auth: ^4.9.0
  google_fonts: ^6.2.1
  http: ^1.1.0
```

## 📋 Pré-requisitos

Antes de começar, você precisará ter instalado em sua máquina:
- [Flutter SDK](https://flutter.dev/docs/get-started/install) (versão 3.0 ou superior)
- [Git](https://git-scm.com/)
- Um editor de código (VS Code, Android Studio, etc.)
- Conta no [Firebase Console](https://console.firebase.google.com/)

## 🔧 Instalação

Siga estas etapas para configurar o projeto localmente:

1. **Clone o repositório**
   ```bash
   git clone https://github.com/seu-usuario/pokedex-flutter-firebase.git
   cd pokedex-flutter-firebase
   ```

2. **Instale as dependências**
   ```bash
   flutter pub get
   ```

3. **Execute o app (após configurar o Firebase)**
   ```bash
   flutter run
   ```

## 🔥 Configuração do Firebase

Para conectar o app ao Firebase:

1. **Crie um projeto no [Firebase Console](https://console.firebase.google.com/)**

2. **Adicione o Firebase ao seu app Flutter**:
   ```bash
   flutter pub add firebase_core
   flutter pub add firebase_auth
   ```

3. **Configure as plataformas**:
   ```bash
   flutterfire configure
   ```
   - Selecione seu projeto Firebase
   - Escolha as plataformas (Android, iOS, Web)

4. **Baixe os arquivos de configuração** e coloque-os nas pastas corretas:
   - Android: `android/app/google-services.json`
   - iOS: `ios/Runner/GoogleService-Info.plist`
   - Web: Adicione a configuração no `index.html`

## 🚀 Executando o Projeto

Para executar o app em modo de desenvolvimento:

1. **Conecte um dispositivo ou inicie um emulador**

2. **Execute o app**:
   ```bash
   flutter run
   ```

3. **Para build de produção**:
   ```bash
   flutter build apk --release  # Para Android
   flutter build ios --release  # Para iOS
   flutter build web --release  # Para Web
   ```

## 📂 Estrutura do Projeto

```
lib/
├── main.dart          # Ponto de entrada da aplicação
├── firebase_options.dart # Configurações do Firebase
└── pages/
    ├── login_page.dart    # Tela de login
    ├── register_page.dart # Tela de cadastro
    └── pokedex.dart       # Tela principal da Pokédex
assets/
├── pokeball.gif       # Ícone animado da Pokébola
├── squirtle1.png      # Imagem para tela de login
└── squirtle2.png      # Imagem para tela de cadastro
