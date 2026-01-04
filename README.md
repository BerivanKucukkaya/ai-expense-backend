# AI Expense Analysis Backend

Bu proje, kullanıcıların aylık harcama verilerini analiz eden ve basit yapay zeka
yaklaşımlarıyla gelecek ay için harcama tahmini yapan bir **FastAPI tabanlı backend servisidir**.

Proje, bütçe kontrolü, harcama alışkanlıklarının analizi ve finansal farkındalık
oluşturmayı amaçlamaktadır.

---

## 🚀 Kullanılan Teknolojiler

- Python 3.10+
- FastAPI
- Pydantic
- NumPy
- Scikit-learn (Linear Regression)
- Uvicorn
- Git & GitHub

---

## 🧠 AI (Yapay Zeka) Bileşeni

Projede yapay zeka şu amaçlarla kullanılmıştır:

- Geçmiş aylara ait harcama verileri kullanılarak  
  **Linear Regression modeli** ile gelecek ayın harcama tahmini yapılır.
- Kullanıcının toplam harcama miktarına göre  
  **risk seviyesi analizi** (Düşük / Orta / Yüksek) gerçekleştirilir.
- Harcama kategorileri analiz edilerek  
  **en çok harcama yapılan kategoriler** belirlenir.

---

## 📡 API Endpoint'leri

### 🔹 `POST /predict-expense`

Geçmiş aylara ait harcama verilerini alır ve bir sonraki ay için tahmini harcamayı döndürür.

**Örnek İstek (JSON):**
```json
{
  "months": [1, 2, 3, 4],
  "expenses": [1200, 1500, 1700, 2000]
}
