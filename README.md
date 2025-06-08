# 🌍 AtmoGuard – Sistema de Alerta para Desastres Naturais

## 📌 Visão Geral

O **AtmoGuard** é um sistema inteligente de monitoramento e alerta de desastres naturais como enchentes, ventos fortes e queimadas. Este projeto visa fornecer informações em tempo real e acessíveis sobre riscos ambientais, transformando dados geográficos e meteorológicos em alertas úteis para a população, gestores públicos e voluntários da Defesa Civil.

Este repositório contém um módulo de simulação que realiza a verificação de alertas ambientais com base na localização do usuário (coordenadas ou endereço), demonstrando uma das funcionalidades centrais do AtmoGuard.

---

## 🧠 Funcionalidades do Código

### 1. **Cálculo de Distância Geográfica**

Utiliza a fórmula de Haversine para calcular a distância (em km) entre dois pontos geográficos com latitude e longitude. Essa métrica é essencial para identificar se um alerta está próximo do usuário (raio de 5 km).

```python
calcular_distancia(lat1, lon1, lat2, lon2)
```

---

### 2. **Geolocalização Reversa**

Faz uso da API do [Nominatim (OpenStreetMap)](https://nominatim.openstreetmap.org/) para converter coordenadas geográficas em um endereço legível.

```python
geolocalizar(latitude, longitude)
```

---

### 3. **Obtenção de Coordenadas por Endereço**

Permite ao usuário inserir um endereço, que é convertido em latitude e longitude via a biblioteca `geopy`.

```python
obter_coordenadas(endereco)
```

---

### 4. **Verificação e Exibição de Alertas**

Simula alertas de desastres próximos à localização do usuário. Se um alerta estiver dentro de um raio de 5 km, ele será exibido com seu tipo e endereço. Também gera um mapa interativo em HTML usando `folium`.

```python
alertasVerify(userLat, userLon)
```

---

### 5. **Interface Simples via Terminal**

O programa solicita ao usuário que informe sua localização por coordenadas ou endereço. Após processar os dados, imprime os alertas no console e salva o mapa gerado como `alertas_mapa.html`.

---

## 🗺️ Mapa Gerado

* Mostra a posição do usuário.
* Exibe o raio de alcance (5 km).
* Destaca os locais com alertas com marcadores vermelhos.
* Permite visualizar tudo interativamente em um navegador web.

---

## 🛠️ Requisitos

* Python 3.8+
* Bibliotecas:

  * `requests`
  * `folium`
  * `geopy`
  * `math` (nativa)

Instalação das dependências:

```bash
pip install requests folium geopy
```

---

## 🚀 Futuras Integrações

Este código é uma simulação e base para futuras versões do AtmoGuard, que incluirão:

* Integração com sensores físicos de campo
* Dados meteorológicos em tempo real (via APIs especializadas)
* Aplicativo móvel
* Suporte offline
* Painel administrativo com monitoramento em tempo real

---

## 💡 Diferencial

O AtmoGuard conecta dados ambientais a ações concretas. Nosso objetivo não é apenas informar, mas **proteger vidas** com tecnologia acessível, confiável e pronta para emergências.

---

## 📄 Licença

Este projeto é de código aberto sob a licença MIT.
