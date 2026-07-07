---
layout: default
title: Getting Started
subtitle: 
---

Claro! Aqui está a página `getting-started.md` pronta em Markdown, com uma estrutura clara e adequada para uso no seu site Jekyll:

---

````markdown
---
layout: page
title: Getting Started
permalink: /projects/
---

# 🧭 Getting Started

This guide walks you through setting up and running the full CST Babybot Tutorial environment inside Docker.

---

## ✅ Step-by-step Setup

### 1. Clone the main project repository

```bash
git clone https://github.com/H-IAAC/cst-tutorial-babybot
mkdir cst-tutorial && cd cst-tutorial
````

---

### 2. Download and build CST-CLI

```bash
git clone https://github.com/CST-Group/CST-CLI
cd CST-CLI
./package.sh
```

➡️ After building, copy the generated `.deb` file to the same directory where your Dockerfile is located.

---

### 3. Build the Docker image

```bash
docker build -t cst-novnc-app .
```

---

### 4. Run the container interactively

```bash
docker run -p 8080:8080 -p 5900:5900 -v ./cst-tutorial/share:/sharevnc -it cst-novnc-app
```

➡️ Then open your browser and go to [http://localhost:8080](http://localhost:8080)
➡️ VNC password: **123456**

---

## 🧪 First Session: Functional Test

Inside the container GUI:

* Open **File System > sharevnc**
* Open a terminal and run:

```bash
./script1.sh
```

### 📜 Contents of `script1.sh`

```bash
thunar /MIMo

cd /sharevnc/1_MIMoCoreModelExample
mkdir -p build
apt-get update && apt-get install -y openjdk-11-jdk

git clone https://github.com/CST-Group/cst.git /opt/cst
cd /opt/cst
./gradlew build
cp /opt/cst/build/libs/*.jar /sharevnc/1_MIMoCoreModelExample/lib/

git clone https://github.com/CST-Group/cst-desktop.git /opt/cst-desktop
cd /opt/cst-desktop
./gradlew build
cp /opt/cst-desktop/build/libs/*.jar /sharevnc/1_MIMoCoreModelExample/lib/

cd /sharevnc/1_MIMoCoreModelExample
javac -encoding UTF-8 -cp "lib/*:src" -d build src/ExperimentMain.java
```

> 🔧 If necessary, to make the script executable:

```bash
chmod +x script1.sh
```

---

## 🧪 Step 2: Run BabyBench Installation Test

Inside the container (via terminal or noVNC):

```bash
conda activate babybench
cd /babybench
python test_installation.py
```

✅ This will generate the folder `results/test_installation/` with a video of the simulation.

---

## 🤖 Step 3: Run the Self-Touch Example

```bash
conda activate babybench
cd /babybench
python examples/random_selftouch.py
```

✅ This initializes MIMo in the `"crib"` scene and runs a test policy with YAML logging.

---

```

