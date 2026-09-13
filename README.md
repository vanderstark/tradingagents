<p align="center">
  <img src="assets/TauricResearch.png" style="width: 60%; height: auto;">
</p>

<div align="center" style="line-height: 1;">
  <a href="https://arxiv.org/abs/2412.20138" target="_blank"><img alt="arXiv" src="https://img.shields.io/badge/arXiv-2412.20138-B31B1B?logo=arxiv"/></a>
  <a href="https://discord.com/invite/hk9PGKShPK" target="_blank"><img alt="Discord" src="https://img.shields.io/badge/Discord-TradingResearch-7289da?logo=discord&logoColor=white&color=7289da"/></a>
  <a href="https://x.com/TauricResearch" target="_blank"><img alt="X Follow" src="https://img.shields.io/badge/X-TauricResearch-white?logo=x&logoColor=white"/></a>
  <a href="https://github.com/vanderstark/tradingagents" target="_blank"><img alt="Komunitas GitHub" src="https://img.shields.io/badge/GitHub_Community-vanderstark-14C290?logo=discourse"/></a>
</div>
<br>
<div align="center">
  <a href="https://github.com/vanderstark/tradingagents" target="_blank"><img alt="TradingAgents #1 Repository of the Day" src="https://trendshift.io/api/badge/repositories/16192" width="250" height="55"/></a>
</div>
<br>
<div align="center">
  <!-- Keep these links. Translations will automatically update with the README. -->
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=de">Deutsch</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=es">Español</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=fr">français</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ja">日本語</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ko">한국어</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=pt">Português</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=ru">Русский</a> | 
  <a href="https://www.readme-i18n.com/TauricResearch/TradingAgents?lang=zh">中文</a>
</div>

---

# TradingAgents: Kerangka Kerja Trading Keuangan Multi-Agen Berbasis LLM

## Berita
- [2026-08] **TradingAgents v0.4.0** rilis dengan perbaikan look-ahead / point-in-time di FRED macro, social sentiment, dan memori decision-log; sinyal keputusan yang lebih jelas; checkpoint resume CLI yang berfungsi; penyelarasan harga Trader; serta model GPT-5.6 dan GLM-5.3. Lihat [CHANGELOG.md](CHANGELOG.md) untuk daftar lengkapnya.
- [2026-07] **TradingAgents v0.3.1** rilis dengan perbaikan kebenaran dan stabilitas: penyaringan look-ahead Alpha Vantage, keamanan crash graph-router, checkpoint resume berbasis bentuk grafik, sumber social sentiment kripto yang berfungsi, anggaran retry LLM yang dapat dikonfigurasi, otentikasi API Key Bedrock, serta dukungan Claude Sonnet 5 / Fable 5.
- [2026-06] **TradingAgents v0.3.0** rilis dengan kontrak akses data yang terverifikasi, regis penyedia yang digalakan (NVIDIA, Kimi, Groq, Mistral, Bedrock, dan titik akhir OpenAI kompatibel), vendor data FRED dan Polymarket, katalog model generasi terbaru, serta gerbang CI.
- [2026-05] **TradingAgents v0.2.5** rilis dengan Sentiment Analyst yang tervalidasi, cakupan model GPT-5.5 dll., dukungan kanal ganda Qwen/GLM/MiniMax, konfigurabilitas `TRADINGAGENTS_*` dengan deteksi otomatis API key, dukungan Ollama jarak jauh, benchmark alpha non-US, serta penanganan path ticker.
- [2026-04] **TradingAgents v0.2.4** rilis dengan agen output terstruktur (Research Manager, Trader, Portfolio Manager), checkpoint resume LangGraph, log keputusan persisten, dukungan penyedia DeepSeek/Qwen/GLM/Azure, Docker, serta perbaikan encoding UTF-8 Windows.
- [2026-03] **TradingAgents v0.2.3** rilis dengan dukungan multi-bahasa, model keluarga GPT-5.4, katalog model terpadu, fiditas tanggal backtesting, serta dukungan proxy.
- [2026-03] **TradingAgents v0.2.2** rilis dengan cakupan model GPT-5.4/Gemini 3.1/Claude 4.6, skala rating lima tiap, API OpenAI Responses, kontrol usaha Anthropic, serta stabilitas lintas platform.
- [2026-02] **TradingAgents v0.2.0** rilis dengan dukungan multi-penyedia LLM (GPT-5.x, Gemini 3.x, Claude 4.x, Grok 4.x) dan arsitekture sistem yang diperbaiki.
- [Trading-R1] **Laporan Teknis](https://arxiv.org/abs/2509.11420) rilis, dengan [Terminal](https://github.com/vanderstark/trading-r1) yang diharapkan segera tersedia.

<div align="center">

🚀 [TradingAgents](#tradingagents-framework) | ⚡ [Instalasi & CLI](#installation-and-cli) | 🎬 [Demo](https://www.youtube.com/watch?v=90gr5lwjIho) | 📦 [Penggunaan Package](#tradingagents-package) | 🤝 [Kontribusi](#contributing) | 📄 [Citation](#citation)

</div>

> 🎉 **TradingAgents** resmi dirilis! Kami telah menerima banyak permintaan tentang pekerjaan ini, dan kami ingin menyampaikan terima kasih atas antusiasme komunitas kami.
>
> Jadi kami memutuskan untuk membuka sumber kode secara penuh. Kami menantikan membangun proyek yang berdampak besar bersama Anda!

## Kerangka Kerja TradingAgents

TradingAgents adalah kerangka kerja trading multi-agen yang menyiriti dinamika perusahaan perdagangan dunia nyata. Dengan mendeploy agen-agen khusus yang didukung LLM: dari analis fundamental, ahli sentimen, dan analis teknis, hingga trader, tim manajemen risiko, platform secara kolaboratif menilai kondisi pasar dan membentuk keputusan perdagangan. Selain itu, agen-agen ini berdebat secara dinamis untuk menentukan strategi optimal.

<p align="center">
  <img src="assets/schema.png" style="width: 100%; height: auto;">
</p>

> Kerangka kerja TradingAgents dirancang untuk tujuan penelitian. Performa perdagangan dapat berbeda tergantung berbagai faktor, termasuk model bahasa penyaji utama yang dipilih, suhu model, periode perdagangan, kualitas data, dan faktor lain yang tidak deterministik. [Tidak dimaksudkan sebagai saran keuangan, investasi, atau perdagangan.](https://tauric.ai/disclaimer/)

Kerangka kerja kami menguraikan tugas perdagangan yang kompleks menjadi peran khusus.

### Tim Analis
- **Analis Fundamental**: Menilai keuangan dan metrik performa perusahaan, mengidentifikasi nilai intrinsik dan tanda bahaya potensial.
- **Analis Sentimen**: Mengagregasi berita headline, StockTwits, dan obrolan Reddit menjadi satu gambaran sentimen untuk menilai suasana hati pasar jangka pendek.
- **Analis Berita**: Memantau berita global dan indikator makro ekonomi, menafsirkan dampak acara pada kondisi pasar.
- **Analis Teknis**: Menggunakan indikator teknis (seperti MACD dan RSI) untuk mendeteksi pola perdagangan dan memprediksi gerakan harga.

<p align="center">
  <img src="assets/analyst.png" width="100%" style="display: inline-block; margin: 0 2%;"></p>

### Tim Penelitian
- Terdiri dari peneliti yang bullish dan bearish yang secara kritis menilai insight yang diberikan oleh Tim Analis. Melalui debat yang terstruktur, mereka menyeimbangkan potensi keuntungan melawan risiko inherent.

<p align="center">
  <img src="assets/researcher.png" width="70%" style="display: inline-block; margin: 0 2%;"></p>

### Agen Trader
- Menyusun laporan dari analis dan peneliti untuk membuat keputusan perdagangan yang diberitahu, menentukan waktu dan magnitudo perdagangan.

<p align="center">
  <img src="assets/trader.png" width="70%" style="display: inline-block; margin: 0 2%;"></p>

### Manajemen Risiko dan Portfolio Manager
- Secara terus-menerus menilai risiko portofolio dengan menilai volatilitas pasar, likuiditas, dan faktor risiko lainnya. Tim manajemen risiko menilai dan menyesuaikan strategi perdagangan, memberikan laporan evaluasi ke Portfolio Manager untuk keputusan akhir.
- Portfolio Manager menyetujui/menolak usulan transaksi. Jika disetujui, pesanan akan dikirim ke bursa tersimulasi dan dieksekusi.

<p align="center">
  <img src="assets/risk.png" width="70%" style="display: inline-block; margin: 0 2%;"></p>

## Instalasi dan CLI

### Instalasi

Kloning TradingAgents:
```bash
git clone https://github.com/vanderstark/tradingagents.git
cd TradingAgents
```

Buat lingkungan virtuall di salah satu environment manager favorit Anda:
```bash
conda create -n tradingagents python=3.12
conda activate tradingagents
```

Instal paket dan dependensinya:
```bash
pip install .
```

### Docker

Secara alternatif, jalankan dengan Docker:
```bash
cp .env.example .env  # tambahkan API key Anda
docker compose run --rm tradingagents
```

Untuk model lokal dengan Ollama:
```bash
docker compose --profile ollama run --rm tradingagents-ollama
```

### API yang Dibutuhkan

TradingAgents mendukung banyak penyedia LLM. Atur API key untuk penyedia pilihan Anda:

```bash
export OPENAI_API_KEY=...          # OpenAI (GPT)
export GOOGLE_API_KEY=...          # Google (Gemini)
export ANTHROPIC_API_KEY=...       # Anthropic (Claude)
export XAI_API_KEY=...             # xAI (Grok)
export DEEPSEEK_API_KEY=...        # DeepSeek
export DASHSCOPE_API_KEY=...       # Qwen — International (dashscope-intl.aliyuncs.com)
export DASHSCOPE_CN_API_KEY=...    # Qwen — China (dashscope.aliyuncs.com)
export ZHIPU_API_KEY=...           # GLM via Z.AI (international)
export ZHIPU_CN_API_KEY=...        # GLM via BigModel (China, open.bigmodel.cn)
export MINIMAX_API_KEY=...         # MiniMax — Global (api.minimax.io)
export MINIMAX_CN_API_KEY=...      # MiniMax — China (api.minimaxi.com)
export OPENROUTER_API_KEY=...      # OpenRouter
export ALPHA_VANTAGE_API_KEY=...   # Alpha Vantage
```

Untuk Azure OpenAI, salin `.env.enterprise.example` ke `.env.enterprise` dan isi kredensialnya.

Untuk AWS Bedrock, instal ekstra dengan `pip install ".[bedrock]"`, set `llm_provider: "bedrock"`, konfigurasikan kredensial AWS (variabel lingkungan, `~/.aws/credentials`, atau peran IAM) dan `AWS_DEFAULT_REGION`, serta gunakan ID model Bedrock, contoh `us.anthropic.claude-opus-4-8-v1:0`.

Untuk model lokal, konfigurasikan Ollama dengan `llm_provider: "ollama"`. Titik akhir baku adalah `http://localhost:11434/v1`; set `OLLAMA_BASE_URL` untuk menunjuk ke `ollama-serve` jarak jauh. Tarik model dengan `ollama pull <name>`, dan pilih "Custom model ID" di CLI untuk model yang tidak tercantum secara default.

Untuk server OpenAI-kompatibel lainnya (vLLM, LM Studio, llama.cpp, atau relay kustom), gunakan `llm_provider: "openai_compatible"` dan set titik akhir melalui `backend_url` (atau `TRADINGAGENTS_LLM_BACKEND_URL`), contoh `http://localhost:8000/v1` untuk vLLM atau `http://localhost:1234/v1` untuk LM Studio. Model adalah apa yang server Anda layani. Tidak ada key yang diperlukan untuk server lokal; set `OPENAI_COMPATIBLE_API_KEY` ketika titik akhir memerlukan.

Secara alternatif, salin `.env.example` ke `.env` dan isi API key Anda:
```bash
cp .env.example .env
```

### Penggunaan CLI

Luncurkan CLI interaktif:
```bash
tradingagents          # perintah yang terinstal
python -m cli.main     # alternatif: jalankan langsung dari sumber
```

Anda akan melihat layar di mana Anda dapat memilih ticker yang diinginkan, tanggal analisis, penyedia LLM, kedalaman penelitian, dan lain-lain.

### Pasar dan Ticker

TradingAgents bekerja dengan pasar mana saja yang ditanggung Yahoo Finance, menggunakan ticker dengan suffix exchange. Identitas perusahaan dan benchmark alpha diselesausi secara otomatis per pasar.

- US: `AAPL`, `SPY`
- Hong Kong: `0700.HK` · Tokyo: `7203.T` · London: `AZN.L`
- India: `RELIANCE.NS`, `.BO` · Kanada: `.TO` · Australia: `.AX`
- China A-shares: Shanghai `.SS`, Shenzhen `.SZ` (contoh `600519.SS` untuk Kweichow Moutai)
- Crypto: `BTC-USD`, `ETH-USD`

<p align="center">
  <img src="assets/cli/cli_init.png" width="100%" style="display: inline-block; margin: 0 2%;"></p>

Antarmuka akan muncul menampilkan hasil seiring mereka dimuat, memungkinkan Anda melacak progres agen saat berjalan.

<p align="center">
  <img src="assets/cli/cli_news.png" width="100%" style="display: inline-block; margin: 0 2%;"></p>

<p align="center">
  <img src="assets/cli/cli_transaction.png" width="100%" style="display: inline-block; margin: 0 2%;"></p>

## Paket TradingAgents

### Detail Implementasi

Kami membangun TradingAgents dengan LangGraph untuk memastikan fleksibilitas dan modularitas. Kerangka kerja ini mendukung banyak penyedia LLM: OpenAI, Google, Anthropic, xAI, DeepSeek, Qwen (Alibaba DashScope, titik akhir internasional dan China), GLM (Zhipu), MiniMax (global + China), OpenRouter, Ollama untuk model lokal, dan Azure OpenAI untuk enterprise.

### Penggunaan Python

Untuk menggunakan TradingAgents di dalam kode Anda, Anda dapat mengimpor modul `tradingagents` dan menginisialisasi objek `TradingAgentsGraph()`. Fungsi `.propagate()` akan mengembalikan keputusan. Anda dapat menjalankan `main.py`, berikut contoh singkatnya:

```python
from tradingagents.graph.trading_graph import TradingAgentsGraph
from tradingagents.default_config import DEFAULT_CONFIG

ta = TradingAgentsGraph(debug=True, config=DEFAULT_CONFIG.copy())

# forward propagate
_, decision = ta.propagate("NVDA", "2026-01-15")
print(decision)
```

Anda juga dapat menyesuaikan konfigurasi baku untuk menetapkan pilihan LLM Anda sendiri, gilingan debat, dll.

```python
from tradingagents.graph.trading_graph import TradingAgentsGraph
from tradingagents.default_config import DEFAULT_CONFIG

config = DEFAULT_CONFIG.copy()
config["llm_provider"] = "openai"        # contoh: openai, google, anthropic, deepseek, groq, ollama; openai_compatible menutupi titik akhir OpenAI kompatibel (vLLM, LM Studio, llama.cpp, ...)
config["deep_think_llm"] = "gpt-5.6"      # Model untuk penalaran kompleks
config["quick_think_llm"] = "gpt-5.6-luna" # Model untuk tugas cepat
config["max_debate_rounds"] = 2

ta = TradingAgentsGraph(debug=True, config=config)
_, decision = ta.propagate("NVDA", "2026-01-15")
print(decision)
```

Lihat `tradingagents/default_config.py` untuk semua opsi konfigurasi.

## Persistensi dan Pemulihan

TradingAgents menyimpan dua jenis status pada setiap eksekusi.

### Log Keputusan

Log keputusan selalu aktif. Setiap eksekusi yang selesai menambahkan keputusannya ke `~/.tradingagents/memory/trading_memory.md`. Pada eksekusi berikutnya untuk ticker yang sama, TradingAgents mengambil return yang telah terrealisasi (bruto dan alpha vs SPY), menghasilkan refleksi satu paragraf, dan memasukkan keputusan yang sama untuk ticker terbaru serta pelajaran lintas-ticker terbaru ke dalam prompt Portfolio Manager, sehingga setiap analisis meneruskan apa yang berhasil dan tidak berhasil.

Override jalurnya dengan `TRADINGAGENTS_MEMORY_LOG_PATH`.

### Checkpoint Resume

Checkpoint resume bersifat opsional melalui `--checkpoint`. Saat diaktifkan, LangGraph menyimpan status setelah setiap node sehingga eksekusi yang crash atau diinterupsi dapat melanjutkan dari langkah terakhir yang berhasil daripada dimulai ulang. Pada eksekusi resume, Anda akan melihat `Resuming from step N for <TICKER> on <date>` dalam log; pada eksekusi baru, Anda akan melihat `Starting fresh`. Checkpoint dihapus secara otomatis pada penyelesaian yang berhasil.

Database SQLite per-ticker hidup di `~/.tradingagents/cache/checkpoints/<TICKER>.db` (override basis dengan `TRADINGAGENTS_CACHE_DIR`). Gunakan `--clear-checkpoints` untuk mengatur ulang semua sebelum eksekusi.

```bash
tradingagents analyze --checkpoint           # aktifkan untuk eksekusi ini
tradingagents analyze --clear-checkpoints    # reset sebelum menjalankan
```

```python
config = DEFAULT_CONFIG.copy()
config["checkpoint_enabled"] = True
ta = TradingAgentsGraph(config=config)
_, decision = ta.propagate("NVDA", "2026-01-15")
```

## Reproduksibilitas

TradingAgents didorong LLM, sehingga dua eksekusi untuk ticker dan tanggal yang sama dapat berbeda. Hal ini diharapkan untuk sebuah alat penelitian yang dibangun di atas model bahasa, bukan defekt. Variasi berasal dari beberapa sumber yang berbeda, dan membantu untuk memisahkannya.

Pengambilan sampel model bahasa bersifat tidak deterministik. Bahkan pada suhu yang tetap, penyedia tidak menjamin output yang identis byte-per-byte di tingka pemanggilan, dan model penalaran (keluarga GPT-5.x standar, dan setiap model dengan mode penulisan) berbeda paling banyak karena penalaran internalnya sendiri yang di-sampling.

Data hidup bergerak. Berita, StockTwits, dan Reddit mengembalikan konten yang berbeda seiring berjalannya waktu, sehingga satu eksekusi hari ini melihat input yang berbeda daripada eksekusi minggu lalu meski untuk tanggal perdagangan historis yang sama. Pin tanggal analisis untuk menahan jendela harga dan indikator tetap, namun sumber sosial dan berita tetap merefleksikan "sekarang".

Untuk mengurangi variasi, Anda dapat menurunkan suhu pengambilan sampel. Set `temperature` di konfigurasi (atau `TRADINGAGENTS_TEMPERATURE` di `.env`); nilai yang lebih rendah membuat model yang menghormatinya menjadi lebih dapat diulang kembali. Model yang dipilih saat ini adalah model generasi berpenalasan dan sebagian besar mengabaikan suhu, sehingga untuk reproduksibilitas yang lebih ketat, gunakan model non-penalasan, yang dapat Anda tetapkan secara eksplisit melalui opsi Custom model ID.

```python
config = DEFAULT_CONFIG.copy()
config["llm_provider"] = "openai"
config["temperature"] = 0.0
# Model penalaran mengabaikan suhu. Untuk reproduksibilitas yang lebih ketat, tetapkan
# model deep/quick non-penalasan secara eksplisit (contoh: melalui opsi Custom model ID).
```

Apa yang tidak lagi berubah: identitas perusahaan yang dianalisis dipecahkan secara deterministik dari ticker sebelum agen berjalan, dan analis pasar menyelaraskan klaim harga dan indikator yang tepat dalam snapshot data yang diverifikasi. Laporan sebelumnya tentang "perusahaan yang berbeda" atau level harga yang dibuat-buat lintas eksekusi ditangani oleh dua mekanisme ini.

Hasil backtesting tidak dijamin cocok dengan angka yang dipublikasikan. Hasil tergantung pada model, suhu, rentang tanggal, kualitas data, dan pengambilan sampel di atas. Perlakukan kerangka kerja sebagai rangka penelitian untuk mempelajari analisis multi-agen, bukan sebagai strategi dengan pengembalian yang tetap.

## Kontribusi

Kontribusi diterima: perbaikan bug, dokumentasi, dan ide fitur; kontribusi sebelumnya dinomori di setiap rilis di [`CHANGELOG.md`](CHANGELOG.md).

## Citation

Harap rujuk pekerjaan kami jika Anda menemukan *TradingAgents* memberikan Anda bantuan:

```
@misc{xiao2025tradingagentsmultiagentsllmfinancial,
      title={TradingAgents: Multi-Agents LLM Financial Trading Framework}, 
      author={Yijia Xiao and Edward Sun and Di Luo and Wei Wang},
      year={2025},
      eprint={2412.20138},
      archivePrefix={arXiv},
      primaryClass={q-fin.TR},
      url={https://arxiv.org/abs/2412.20138}, 
}
```