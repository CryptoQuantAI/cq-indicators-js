# 📦 cq-indicators-js
### Technical Indicators for JavaScript & TypeScript  
Part of the **CryptoQuantAI** Ecosystem

`cq-indicators-js` is the JavaScript/TypeScript version of the `cq-indicators` package, providing  
a fast, lightweight, and easy-to-use library of technical indicators for:

- Trading bots  
- Web dashboards  
- Chart overlays  
- Data analysis pipelines  
- Node.js and browser environments  

This library is fully compatible with:
- **cq-ohlcv-js** (optional future module)
- **cq-tradingview-js**
- Any OHLCV-formatted arrays or objects

---

## 🚀 Features

- ✅ 60+ technical indicators  
- ✅ Pure JavaScript (no native dependencies)  
- ✅ TypeScript definitions included  
- ✅ Works in Node.js & browser  
- ✅ Lightweight & fast (optimized loops)  
- ✅ Compatible with arrays, OHLCV objects, and custom data feeds  
- ✅ Easy chaining and functional API  

Includes:
- SMA, EMA, WMA, HMA  
- RSI, Stochastic, CCI  
- ATR, Bollinger Bands  
- MACD, SuperTrend  
- Crypto‑specific indicators (Volatility, Funding Metrics*)  

\* (Funding-based indicators available only when data provided)

---

## 📦 Installation

```bash
npm install cq-indicators-js
```

or with yarn:

```bash
yarn add cq-indicators-js
```

---

## 💡 Quick Start

### ✅ Import and use indicators

```javascript
import { ema, rsi } from "cq-indicators-js";

const closes = [100, 102, 101, 103, 104];

const ema9 = ema(closes, 9);
const rsi14 = rsi(closes, 14);

console.log(ema9);
console.log(rsi14);
```

---

## ✅ OHLCV Example

```javascript
import { macd } from "cq-indicators-js";

const candles = [
  { open: 100, high: 102, low: 99, close: 101, volume: 200 },
  { open: 101, high: 103, low: 100, close: 102, volume: 180 },
  // ...
];

const closePrices = candles.map(c => c.close);

const macdData = macd(closePrices);

console.log(macdData);
```

---

## ✅ Multi‑Indicator Example

```javascript
import { ema, bollinger, atr } from "cq-indicators-js";

const closes = candles.map(c => c.close);

const out = {
  ema9: ema(closes, 9),
  ema21: ema(closes, 21),
  bb20: bollinger(closes, 20),
  atr14: atr(candles, 14)
};

console.log(out);
```

---

## 🗂 Folder Structure

```
cq-indicators-js/
│
├── src/
│   ├── index.ts
│   ├── ema.ts
│   ├── sma.ts
│   ├── macd.ts
│   ├── rsi.ts
│   ├── atr.ts
│   ├── bollinger.ts
│   ├── types.ts
│   └── utils/
│       ├── math.ts
│       ├── smoothing.ts
│
├── dist/
├── tests/
└── README.md
```

---

## 📅 Roadmap

- ✅ Release core indicators  
- ✅ Add TypeScript generics  
- ⏳ Add Polars‑JS and Apache Arrow support  
- ⏳ GPU acceleration (WebGPU when stable)  
- ⏳ Streaming indicators for real‑time dashboards  

---

## 🤝 Contributing

We welcome contributions:

- Add new indicators  
- Improve performance  
- Expand TypeScript support  
- Browser optimizations  

Please follow:
- ESLint rules  
- Prettier formatting  
- TypeScript strict mode  

---

## ⚖️ License

MIT License — free for commercial and personal use.

---

## 👨‍💻 Maintained By

CryptoQuantAI Development Team
