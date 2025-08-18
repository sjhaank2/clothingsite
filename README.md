# clothingsite
Clothing website with index.html

# Semantic Search Test Queries for Google Agent SDK

## 🎯 Test Setup Verification
**Website:** TestWebsite with 5 products (ProductA-ProductE)  
**Tool:** Google Agent SDK  
**Goal:** Verify true semantic understanding vs keyword matching

---

## ❄️ COLD WEATHER QUERIES (Should return ProductA & ProductB)

### Primary Tests:
```
"What should I wear when it's freezing outside?"
"I need warm clothing for winter"
"Show me thermal wear for cold weather"
"What clothing keeps you warm in snow?"
"I'm looking for winter jackets and coats"
```

### Advanced Semantic Tests:
```
"Clothing for sub-zero temperatures"
"What to wear in arctic conditions" 
"I need insulation against the cold"
"Professional attire for cold office"
"Business clothing for chilly weather"
```

**Expected Results:** ProductA (thermal technology, sub-zero) & ProductB (business, office)  
**Keyword Check:** NO "warm", "winter", "cold weather" exist on website

---

## ☔ WET WEATHER QUERIES (Should return ProductC)

### Primary Tests:
```
"What should I wear in the rain?"
"I need protection from getting wet"
"Show me gear that keeps you dry"
"Clothing for rainy season"
"What to wear during storms?"
```

### Advanced Semantic Tests:
```
"Protection from heavy downpours"
"Gear for monsoon season"
"Clothing that repels water"
"What to wear in precipitation?"
"Storm-resistant clothing options"
```

**Expected Results:** ProductC (waterproof, stormy weather, precipitation)  
**Keyword Check:** NO "rain", "wet weather", "dry" exist on website

---

## 🏔️ OUTDOOR ADVENTURE QUERIES (Should return ProductD)

### Primary Tests:
```
"What shoes should I wear for hiking?"
"I need footwear for mountain climbing"
"Show me boots for outdoor adventures"
"Shoes with good grip for trails"
"What to wear for rock climbing?"
```

### Advanced Semantic Tests:
```
"Footwear for alpine expeditions"
"Shoes for rocky terrain navigation"
"Mountain climbing equipment"
"Trekking gear for trails"
"Footwear with superior traction"
```

**Expected Results:** ProductD (mountain trails, alpine adventures, traction)  
**Keyword Check:** NO "hiking", "outdoor", "climbing" exist on website

---

## ☀️ HOT WEATHER QUERIES (Should return ProductE)

### Primary Tests:
```
"What should I wear in hot summer weather?"
"I need cooling clothing for heat"
"Show me clothes for beach vacation"
"What to wear in hot climates?"
"Clothing that keeps you cool"
```

### Advanced Semantic Tests:
```
"Apparel for tropical destinations"
"Clothing for sweltering heat"
"What to wear in high temperatures?"
"Breathable clothes for humidity"
"Lightweight clothing for hot days"
```

**Expected Results:** ProductE (tropical climates, sweltering conditions, breathable)  
**Keyword Check:** NO "summer", "hot weather", "cool", "beach" exist on website

---

## 🔄 CROSS-CATEGORY QUERIES

### Weather Protection:
```
"What clothing protects from weather?"
"Show me all-weather gear"
"Clothing for different climates"
"Weather-resistant clothing options"
```

### Professional/Business:
```
"What should I wear to business meetings?"
"Professional clothing options"
"Office-appropriate outerwear"
"Corporate attire for different seasons"
```

### Adventure/Activity:
```
"Gear for outdoor activities"
"Clothing and footwear for adventures"
"Equipment for mountain activities"
"What to wear for outdoor sports?"
```

---

## 🧠 CONVERSATIONAL/NATURAL QUERIES

### Intent-Based Questions:
```
"I'm going to Alaska next month, what should I pack?"
"I have an important client meeting in a cold office"
"I'm planning a tropical vacation, what clothes do I need?"
"I'll be hiking in the mountains, what footwear is best?"
"It's been raining a lot, what should I wear outside?"
```

### Problem-Solution Queries:
```
"I always get cold at work, what can I wear?"
"I get soaked walking to my car, any solutions?"
"My feet slip on rocky trails, what shoes help?"
"I overheat easily in hot weather, what clothing helps?"
"I need something professional but warm"
```

---

## ✅ SUCCESS CRITERIA

### **PASS (True Semantic Search):**
- Returns correct products despite missing exact keywords
- Understands intent and context
- Maps concepts to relevant products

### **FAIL (Keyword Matching Only):**
- Only returns results when exact words are found
- Misses relevant products due to terminology gaps
- Requires exact phrase matching

---

## 📊 TESTING METHODOLOGY

### 1. Ask Query via Google Agent SDK
```python
response = agent.search(query="I need warm clothing for winter")
```

### 2. Check Results
- Which products were returned?
- Are they semantically relevant?
- Check website for exact keyword matches

### 3. Verify Semantic Understanding
- Query: "warm clothing" 
- Expected: ProductA & ProductB
- Verification: Search website for "warm" = NOT FOUND
- Result: ✅ True semantic search confirmed!

### 4. Document Results
- Query → Products Returned → Keyword Match Status
- Build evidence of semantic vs keyword capabilities

---

## 🎯 QUICK VERIFICATION TESTS

### Must-Pass Semantic Tests:
1. **"warm clothing"** → ProductA & ProductB (no "warm" on site)
2. **"rain protection"** → ProductC (no "rain" on site)  
3. **"hiking boots"** → ProductD (no "hiking" on site)
4. **"summer clothes"** → ProductE (no "summer" on site)

If these 4 tests pass, your semantic search is working! 🎉
