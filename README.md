# Diagram-Keluarga-Kecerdasan-Buatan
UAS KECERDASAN BUATAN

```python
import matplotlib.pyplot as plt
import networkx as nx

# Membuat graf kosong untuk pohon keluarga
G = nx.DiGraph()

# Menambahkan node ke dalam graf sesuai pohon keluarga
nodes = {
    "Hadi": (0, 4), "Retno": (2, 4),
    "Bayu": (-2, 3), "Desi": (0, 3), "Wahyu": (2, 3),
    "Rina": (4, 3), "Ardi": (6, 3),
    "Naufal": (-2, 2), "Eurasia": (0, 2), "Nurul": (1, 2),
    "Yanto": (3, 2), "Hamzah": (5, 2),
    "Eka": (4, 2), "Mira": (6, 2), "Bastian": (7, 2),
    "Wanda": (-2, 1), "Aji": (1, 1), "Gunawan": (3, 1),
    "Anggun": (5, 1), "Boy": (7, 1)
}

# Tambahkan node ke graf
for name, pos in nodes.items():
    G.add_node(name, pos=pos)

# Menambahkan hubungan antar node (edges)
edges = [
    ("Hadi", "Bayu"), ("Hadi", "Desi"), ("Hadi", "Wahyu"), ("Hadi", "Rina"), ("Hadi", "Ardi"),
    ("Retno", "Bayu"), ("Retno", "Desi"), ("Retno", "Wahyu"), ("Retno", "Rina"), ("Retno", "Ardi"),
    ("Bayu", "Naufal"), ("Desi", "Eurasia"), ("Desi", "Nurul"),
    ("Wahyu", "Yanto"), ("Rina", "Hamzah"),
    ("Eka", "Anggun"), ("Mira", "Boy"), ("Ardi", "Bastian"),
    ("Naufal", "Wanda"), ("Nurul", "Aji"), ("Yanto", "Gunawan")
]

# Tambahkan edges ke graf
G.add_edges_from(edges)

# Mendapatkan posisi node
pos = nx.get_node_attributes(G, 'pos')

# Menggambar graf
plt.figure(figsize=(10, 8))
nx.draw(G, pos, with_labels=True, node_size=3000, node_color="lightblue", font_size=10, font_weight="bold")
plt.title("Pohon Keluarga Sederhana", fontsize=14)
plt.show()
```
Hasil output :
![image](https://github.com/user-attachments/assets/b0176ef7-059d-4433-b4d0-44c50241d8ee)
![image](https://github.com/user-attachments/assets/1f02d79e-95a1-43f4-8be1-908a995f04cb)


