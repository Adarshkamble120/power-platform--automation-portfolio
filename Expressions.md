# Power Automate Expressions Used

## 🎂 Birthday Check
formatDateTime(items('Apply_to_each')?['DateOfBirth'], 'MM-dd')  
equals(formatDateTime(utcNow(),'MM-dd'))

---

## 📅 Anniversary Check
formatDateTime(items('Apply_to_each')?['JoiningDate'], 'MM-dd')

---

## ⚠️ Fraud Threshold Condition
greater(int(items('Apply_to_each')?['RiskScore']), 75)

---

## 📊 Null Handling
coalesce(triggerOutputs()?['body/EmployeeName'], 'Unknown')

---

## 🕒 Current Date
utcNow()

---

## 🔁 Escalation Delay
addDays(utcNow(),2)
