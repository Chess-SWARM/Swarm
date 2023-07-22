# SWRAM Application

The swarm application is a Chess tournament planning application.

## Tech Stack

### Front-end :

- [Nuxt 3](https://nuxt.com/docs)
- [Vuetify](https://vuetifyjs.com/en/components/all/)

### Back-end :

- [Spring boot 3](https://docs.spring.io/spring-boot/docs/current/reference/htmlsingle/)

### Database :

- PostGreSQL

### External tools

- Teamcity as CI/CD (Self-hosted)
- YouTrack as Project Management (Cloud)

## Project Structure :

```
SWARM
├── 🗂️ Back
│   ├── 📁 api/
│   ├── 📁 core/
│   ├── 📁 ws/
│   └── ⚙️ pom.xml
│
├── 🗂️ Front
│   └── ⚙️ package.json
│
└── 🗂️ Infra 
    ├── 📁 dev
    │   └── 📦docker-compose.yml
    └── 📁 prod
        └── 📦docker-compose.yml
```

## Project setup

### 0. Requirement :

- [*Java JDK 17+*](https://jdk.java.net/archive/)
- [*Node 16.10.0+*](https://nodejs.org/en)
- *Docker*

And clone project :

```shell
git clone https://github.com/Chess-SWARM/Swarm.git
```

### 1. Starts containers

Starting a PostGreSQL instance.

```shell
docker compose -f /Infra/dev/docker-compose.yml up -d
```

### 2. Back

Download all maven dependencies and generate classes

```shell
cd Back
mvn clean install -Dmaven.test.skip=true
```

*_Note_ : Skip tests for the first install*

**Run with :**

```shell

```

**Url :** [localhost:8080](http://localhost:8080)

### 3. Front

download all package for the front-end

```shell
npm install
```

**Run with :**

```bash
npm run dev
```

**Url :** [localhost:3000](http://localhost:3000)


## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
