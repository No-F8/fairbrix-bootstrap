# Fairbrix Bootstrap

Bootstrap files for the **Fairbrix blockchain**, taken from a fully synced NitroPool full relay node.  
These files allow new wallets and nodes to skip the slow initial block download (IBD) and get synced much faster.

---

## 📦 Contents
Each release includes:
- `blocks/` — blockchain block files
- `chainstate/` — current chain state
- `peers.dat` — known peers to help your node connect quickly
- Provided in both:
  - **Linux**: `.tar.gz` archive
  - **Windows**: `.zip` archive

---

## 🚀 How to Use

### Linux
1. Stop your Fairbrix node if it’s running:
   ```
   fairbrix-cli stop
   ```

2. Navigate to your data directory and extract the bootstrap:
   ```
   cd ~/.fairbrix
   tar -xvzf fairbrix-bootstrap-YYYY-MM-DD.tar.gz -C ~/.fairbrix
   ```

3. Restart your node:
   ```
   fairbrixd -daemon
   ```

### Windows
1. Close Fairbrix Core if it’s running.
2. Navigate to your data folder (default path):
    `C:\Users\<YourName>\AppData\Roaming\Fairbrix`
3. Extract the contents of the provided `.zip` archive into a new `Fairbrix` folder.
4. Restart Fairbrix Core and it will sync from the bootstrap.

---

## ⚠️ Notes
- Always **backup your `wallet.dat`** before replacing blockchain data.
- If peers fail to connect, you can manually add nodes in your `fairbrix.conf`:

  **NitroPool addnode:**
  ```
  addnode=51.75.117.211:8591
  ```

  **DNS Seeds**
  ```
  addnode=fbx.kawaii.casa
  addnode=fairbrix.dnsseed.multicoin.co
  ```

- Bootstrap files are **point-in-time snapshots**. Your node will still need to download and verify blocks after the snapshot date.

---

## 📡 Source
- Snapshot created from a **NitroPool full relay node**.
- Updated periodically to help new users join the network quickly.

---

## ⬇️ Latest Download
You can always find the latest bootstrap files under the **Releases** page:

[![GitHub release (latest by date)](https://img.shields.io/github/v/release/No-F8/fairbrix-bootstrap?label=Latest%20Release)](https://github.com/No-F8/fairbrix-bootstrap/releases/latest)
