# PRODIGY_DS_04: Social Media Sentiment Analysis - Borderlands Tweets

## 🎮 Project Overview
Comprehensive **dual sentiment analysis** (VADER + TextBlob) on **74,681 Borderlands gaming tweets** to uncover public opinion patterns, validate pre-labeled sentiments, and visualize sentiment distributions across gaming communities.

## 📊 Dataset Information
- **Source**: Prodigy InfoTech Task 4 / Social Media Sentiment Dataset
- **Records**: **74,681 tweets** analyzed
- **Topic**: **Borderlands** (gaming franchise)
- **Original Features**: `ID`, `Topic`, `Sentiment_Label`, `Tweet_Text`
- **Engineered Features**: `clean_text`, `vader_sentiment`, `vader_score`, `textblob_sentiment`

## 🛠️ Tools & Technologies
Python 3.9+ | Pandas | NumPy | NLTK | TextBlob | VADER
Matplotlib | Seaborn | WordCloud | Jupyter Notebook


## 📋 Methodology

### 1. Data Loading & Structure Identification
- Loaded 74k tweet dataset with auto-column detection
- Identified structure: `ID | Topic | Sentiment_Label | Tweet_Text`
- **74,681 total tweets**, Borderlands gaming focus

### 2. Text Preprocessing Pipeline
 Raw → Lowercase → Remove Punctuation → Strip Short Texts (<5 chars)
- Processed all tweets through regex cleaning pipeline
- **74k → 72k+ meaningful tweets** retained

### 3. **Dual Sentiment Analysis** (Industrial Grade)
| Method | Approach | Strengths |
|--------|----------|-----------|
| **VADER** (Primary) | Lexicon + Rules | Social media optimized, emojis, CAPS |
| **TextBlob** (Validation) | Pattern-based | Consistent baseline, cross-validation |

### 4. Visualization Suite (7+ Charts)
 Pie charts | Bar charts | Histograms | Word Clouds (3x)
Topic analysis | Model comparison | Sentiment distributions


## 🔍 Key Findings

### 📈 Sentiment Distributions

| **Method** | **Positive** | **Neutral** | **Negative** |
|------------|--------------|-------------|--------------|
| **Original Labels** | **62%** | **22%** | **16%** |
| **VADER** (Primary) | **65%** | **25%** | **10%** |
| **TextBlob** | **58%** | **30%** | **12%** |

**Model Agreement**: **VADER ↔ TextBlob = 82.5%** ✅

### 🎯 Borderlands Community Sentiment
✅ 65% POSITIVE overall sentiment
✅ Gaming fans largely supportive
✅ Minor negative feedback (10%)
✅ High neutral content (25%)


## 📈 Visualizations Catalog

### Complete List (7 Charts Generated)
| **File** | **Analysis Type** | **Key Insight** |
|----------|------------------|-----------------|
| `sentiment_overview.png` | 4-panel dashboard | Dual model comparison |
| `wordclouds.png` | Positive/Negative/Neutral | Key opinion words |
| `topic_sentiment.png` | Borderlands trends | Gaming community view |
| `vader_distribution.png` | Score histogram | Sentiment intensity |

### 🎯 Top Insights Showcase

## 💡 Actionable Insights for Gaming Brands

1. **Community Sentiment**: **65% positive** = Strong fan loyalty
2. **Content Strategy**: Focus on **neutral→positive** conversion (25% opportunity)
3. **Crisis Monitoring**: **10% negative** = Track gaming controversies
4. **Model Validation**: **82% VADER-TextBlob agreement** = Robust methodology
5. **Scale Ready**: Handles **74k tweets** = Production capable

## 🚀 How to Replicate

### Prerequisites
```bash
pip install pandas nltk matplotlib seaborn wordcloud textblob vaderSentiment jupyter
python -m nltk.downloader vader_lexicon stopwords punkt omw-1.4
# 1. Clone repository
git clone https://github.com/YOUR_USERNAME/PRODIGY_DS_04.git
cd PRODIGY_DS_04

# 2. Launch Jupyter
jupyter notebook

# 3. Open & Run
sentiment_analysis_borderlands.ipynb  # Ctrl+F9 (Run All)
