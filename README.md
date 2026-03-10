# n8n
## **1. Install via npm (Node.js required)**

### **Step 1: Install Node.js**

n8n requires **Node.js 18 or 20** (LTS recommended). Since you’re on macOS:

```bash
brew install node@20
```

Or download from [Node.js official site](https://nodejs.org/).

Check version:

```bash
node -v
npm -v
```

---

### **Step 2: Install n8n globally**

```bash
npm install -g n8n
```

Check installation:

```bash
n8n --version
```

---

### **Step 3: Run n8n**

```bash
n8n
```

By default, it runs on:

```
http://localhost:5678
```

Open in your browser to access the UI.

---

## **2. Install via Docker (recommended for isolation)**

If you have Docker installed:

```bash
docker run -it --rm \
  -p 5678:5678 \
  -v ~/.n8n:/home/node/.n8n \
  n8nio/n8n
```

* `-p 5678:5678` → maps the port
* `-v ~/.n8n:/home/node/.n8n` → saves workflow data

---

## **3. Optional: Start n8n as a service (auto start)**

For macOS using `brew services`:

```bash
brew install n8n
brew services start n8n
```

Or use **pm2** to keep it running:

```bash
npm install -g pm2
pm2 start n8n
pm2 save
```

---

✅ After this, n8n will be running and you can start building automation workflows.