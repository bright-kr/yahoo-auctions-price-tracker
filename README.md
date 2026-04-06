# Yahoo! Auctions Japan 가격 추적기

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-blue?style=flat-square)](https://brightdata.co.kr)
[![Yahoo! Auctions Japan Price Tracker](https://img.shields.io/badge/Yahoo!%20Auctions%20Japan%20Price%20Tracker-Managed%20Solution-orange?style=flat-square)](https://brightdata.co.kr/products/insights/price-tracker/yahoo-auctions)
[![Python](https://img.shields.io/badge/Python-3.9%2B-yellow?style=flat-square)](https://python.org)

[![Bright Insights Price Tracker](https://raw.githubusercontent.com/danielshashko/bright-insights-assets/main/price-tracker-hero-v2.png)](https://brightdata.co.kr/products/insights/price-tracker/yahoo-auctions)

실시간 Yahoo! Auctions Japan 가격 추적 - 일본 최대 온라인 경매 플랫폼. 시작하는 방법은 두 가지입니다: **완전 관리형** 인텔리전스 플랫폼 또는 Bright Data의 AI Scraper Builder로 구축한 **커스텀 scraper**.

---

## 옵션 1: Bright Insights - AI 기반 가격 추적 (권장)

**[Bright Insights](https://brightdata.co.kr/products/insights/price-tracker/yahoo-auctions)**는 Bright Data의 완전 관리형 리테일 인텔리전스 플랫폼입니다. scraper를 구축할 필요도, 인프라를 유지할 필요도 없습니다. 구조화되고 분석 준비가 완료된 가격 데이터가 대시보드, 데이터 피드 또는 BI 도구로 바로 제공됩니다.

**팀이 Bright Insights를 선택하는 이유:**
- 🚀 **설정 불필요** - 즉시 사용 가능한 대시보드와 데이터 피드로 몇 분 안에 운영 시작
- 🤖 **AI 기반 추천** - 대화형 AI 어시스턴트가 수백만 개의 데이터 포인트를 즉시 실행 가능한 인사이트로 전환
- ⚡ **실시간 모니터링** - 시간 단위부터 일 단위까지의 새로고침 주기와 즉시 알림 제공 (email, Slack, webhook)
- 🌍 **무제한 확장성** - 모든 웹사이트, 모든 지역, 모든 새로고침 주기 지원
- 🔗 **플러그 앤 플레이 통합** - AWS, GCP, Databricks, Snowflake 등 지원
- 🛡️ **완전 관리형** - Bright Data가 schema 변경, 사이트 업데이트, 데이터 품질을 자동으로 처리

**주요 사용 사례:**
- ✅ 모든 제품 카테고리에서 **Yahoo! Auctions Japan 가격 모니터링**
- ✅ **재고 수준 및 가용성 추적** 실시간 지원
- ✅ 관심 있는 제품에 대한 **가격 알림 설정**
- ✅ MAP 정책 준수 모니터링 및 가격 위반 감지
- ✅ 경쟁사 프로모션 및 프로모션 동향 추적
- ✅ 정제되고 표준화된 데이터를 동적 가격 책정 알고리즘 또는 AI 모델에 직접 공급

> **월 $250부터 - [맞춤 견적 받기 →](https://brightdata.co.kr/products/insights/price-tracker/yahoo-auctions)**

---

## 옵션 2: 직접 Yahoo! Auctions Japan Scraper 구축하기

사전 구축된 Yahoo! Auctions Japan scraper API가 없나요? 문제없습니다. Bright Data의 **AI Scraper Builder**는 몇 번의 클릭만으로 커스텀 Yahoo! Auctions Japan scraper를 생성합니다 — 코딩이 필요 없습니다.

### 몇 분 만에 Yahoo! Auctions Japan scraper 구축하기

**[Yahoo! Auctions Japan AI Scraper Builder 열기 →](https://brightdata.co.kr/products/web-scraper/yahoo-auctions)**

도메인을 선택하고, 필요한 데이터 요구사항을 설명하면, AI scraper builder가 자동으로 API를 생성합니다.

1. **일반 영어로 데이터 요구사항 설명**
2. **AI가 즉시 scraper API 생성**
3. **즉시 결과를 위해 API 요청 실행**
4. 필요한 경우 **내장 IDE에서 코드 편집**

구축이 완료되면 scraper에 **Web Scraper ID** (`gd_xxxxxxxxxxxx`)가 부여됩니다 — 아래 Setup 단계에서 사용할 수 있도록 복사해 두세요.

### 사전 요구사항

- Python 3.9 이상
- [Bright Data 계정](https://brightdata.co.kr) (무료 체험 가능)
- Bright Data **API token** ([발급 방법](https://docs.brightdata.co.kr/general/account/account-settings#api-token))
- Yahoo! Auctions Japan용 **Web Scraper ID** (위의 구축 단계에서 획득)

### Setup

1. **이 repository 복제**

   ```bash
   git clone https://github.com/bright-kr/yahoo-auctions-price-tracker.git
   cd yahoo-auctions-price-tracker
   ```

2. **의존성 설치**

   ```bash
   pip install -r requirements.txt
   ```

3. **자격 증명 구성**

   `.env.example`을 `.env`로 복사한 뒤 값을 입력하세요:

   ```bash
   cp .env.example .env
   ```

   ```env
   BRIGHTDATA_API_TOKEN=your_api_token_here
   BRIGHTDATA_DATASET_ID=your_dataset_id_here
   ```

   > **Web Scraper ID**
   > [AI Scraper Builder dashboard](https://brightdata.co.kr/products/web-scraper/yahoo-auctions)에서 Web Scraper ID를 복사해
   > `BRIGHTDATA_DATASET_ID`에 붙여 넣으세요 (형식: `gd_xxxxxxxxxxxx`).

---

## 사용법

Yahoo! Auctions Japan scraper를 구축하고 `.env`에 Web Scraper ID를 구성하면, Python 인터페이스는 동일한 방식으로 작동합니다:

### 1. URL로 특정 제품 추적

구조화된 가격 데이터를 가져오기 위해 Yahoo! Auctions Japan 제품 URL 목록을 전달합니다:

```python
from price_tracker import track_prices

urls = [
    "https://www.auctions.yahoo.co.jp/product/sample-item-123456",
    # Add more product URLs here
]

results = track_prices(urls)
for item in results:
    print(f"{item.get('title')} - {item.get('final_price', item.get('price'))} {item.get('currency', '')}")
```

또는 직접 실행:

```bash
python price_tracker.py
```

### 2. 키워드로 제품 검색

키워드 검색과 일치하는 제품을 찾습니다:

```python
from price_tracker import discover_by_keyword

results = discover_by_keyword("laptop", limit=50)
```

### 3. 카테고리 URL로 제품 탐색

Yahoo! Auctions Japan 카테고리 페이지의 모든 제품을 수집합니다:

```python
from price_tracker import discover_by_category

results = discover_by_category(
    "https://auctions.yahoo.co.jp/category/example",
    limit=100,
)
```

---

## 출력 필드

각 결과 레코드에는 다음 필드가 포함됩니다:

| Field | Description |
|-------|-------------|
| `url` | 제품 페이지 URL |
| `title` | 제품명 / 제목 |
| `brand` | 브랜드 또는 제조사 |
| `initial_price` | 원래 가격 / 정가 |
| `final_price` | 현재 판매 가격 |
| `currency` | 통화 코드 (예: USD, EUR) |
| `discount` | 할인 금액 또는 할인율 |
| `in_stock` | 상품의 구매 가능 여부 |
| `rating` | 평균 별점 |
| `reviews_count` | 총 리뷰 수 |
| `seller_name` | 판매자 이름 |
| `images` | 제품 이미지 URL 배열 |
| `description` | 제품 설명 텍스트 |
| `timestamp` | 데이터 수집 타임스탬프 |

### 샘플 출력

```json
[
  {
    "url": "https://www.auctions.yahoo.co.jp/product/sample-item-123456",
    "title": "Example Product Name",
    "brand": "Example Brand",
    "initial_price": 59.99,
    "final_price": 44.99,
    "currency": "USD",
    "discount": "25%",
    "in_stock": true,
    "rating": 4.5,
    "reviews_count": 1234,
    "images": ["https://auctions.yahoo.co.jp/images/product1.jpg"],
    "description": "Product description text...",
    "timestamp": "2025-01-15T10:30:00Z"
  }
]
```

---

## 고급 옵션

`trigger_collection()` 함수는 데이터 수집을 제어하기 위한 선택적 파라미터를 지원합니다:

| Parameter | Type | Default | Description |
|-----------|------|---------|-------------|
| `limit` | integer | - | 반환할 최대 레코드 수 |
| `include_errors` | boolean | `true` | 결과에 오류 리포트 포함 |
| `notify` | string (URL) | - | 스냅샷 준비 완료 시 호출할 webhook URL |
| `format` | string | `json` | 출력 형식: `json`, `csv` 또는 `ndjson` |

옵션 사용 예시:

```python
from price_tracker import trigger_collection, get_results

inputs = [{"url": "https://www.auctions.yahoo.co.jp/product/sample-item-123456"}]
snapshot_id = trigger_collection(inputs, limit=200, notify="https://your-webhook.com/hook")
results = get_results(snapshot_id)
```

---

## 리소스

- 🌟 [Yahoo! Auctions Japan Price Tracker - Bright Insights (Managed)](https://brightdata.co.kr/products/insights/price-tracker/yahoo-auctions)
- 🏗️ [Yahoo! Auctions Japan Scraper 구축하기](https://brightdata.co.kr/products/web-scraper/yahoo-auctions)
- 📖 [Bright Data Web Scraper API 문서](https://docs.brightdata.co.kr/scraping-automation/web-scraper-api/overview)
- 🗄️ [Web Scrapers Control Panel](https://brightdata.co.kr/cp/scrapers)
- 🔑 [API token 발급 방법](https://docs.brightdata.co.kr/general/account/account-settings#api-token)
- 🌐 [Bright Data 홈페이지](https://brightdata.co.kr)

---

*[Bright Data](https://brightdata.co.kr)로 구축 - 업계를 선도하는 웹 데이터 플랫폼.*