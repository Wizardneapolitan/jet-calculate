# Jet Pricing API ✈️

Questa API calcola il prezzo stimato di un volo privato tra due aeroporti, usando dati reali di jet memorizzati in Supabase.

## 📁 Endpoints

### `GET /api/ping`
Verifica se l'API è attiva.

**Risposta attesa:**
```json
{ "message": "pong ✅" }
```

### `POST /api/calculate`
Calcola il prezzo stimato del volo.

**Body JSON:**
```json
{
  "departure": "LIML",
  "arrival": "LFPB",
  "pax": 4
}
```

**Risposta esempio:**
```json
{
  "jets": [
    {
      "jet_id": "jet001",
      "model": "Phenom 300",
      "home_base": "LIML",
      "distance_km": 638,
      "flight_time_h": "1.13",
      "price": 4800
    }
  ]
}
```

---

## ⚙️ Struttura

- `/api/ping.js` – Funzione di test
- `/api/calculate.js` – Logica di pricing e calcolo tempo volo
- `package.json` – Configurazione per Vercel

## 🚀 Deployment
Distribuito tramite [Vercel](https://vercel.com)
