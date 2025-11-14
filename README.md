# 🚀 AWS Static Website – S3 + CloudFront (CDN)

Host a fully static website using **Amazon S3** and deliver it globally at high speed using **Amazon CloudFront**.
This project demonstrates **real AWS architecture**, **cache invalidation workflows**, and **Git/GitHub version control**, making it an excellent cloud engineering portfolio piece.

---

## 📸 Project Screenshot

<img width="824" height="315" alt="Screenshot 2025-11-14 at 10 22 09" src="https://github.com/user-attachments/assets/43fbec5f-1952-4bc3-bbe2-460b44b5fce0" />


---

## 🌍 Live CloudFront URL

Your site is deployed globally via AWS CloudFront:

👉 **[https://d31z5mdzs5x5ee.cloudfront.net](https://d31z5mdzs5x5ee.cloudfront.net)**

---

## 🔧 Tech Used

### **Frontend**

* HTML5
* CSS3

### **AWS Services**

* **Amazon S3** (Static Website Hosting)
* **Amazon CloudFront** (Global CDN)
* **AWS IAM** (Permissions for S3 & CloudFront access)

### **Developer Tools**

* **Visual Studio Code**
* **Git & GitHub**
* **AWS Console**

---

## 📁 Project Structure

```
aws-static-website-s3/
│
├── index.html           # main webpage
├── styles.css           # page styling
└── README.md            # project documentation
```

---

## 🚀 How to Deploy This (Step-by-Step)

### **1️⃣ Create an S3 Bucket**

* Block all public access → OFF
* Enable **static website hosting**
* Upload `index.html` & `styles.css`

### **2️⃣ Add a Bucket Policy**

Allow public reads:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::fausto-static-site-s3/*"
    }
  ]
}
```

### **3️⃣ Create CloudFront Distribution**

* Origin: your S3 static site URL
* Default root object: `index.html`
* Leave WAF disabled (optional)

### **4️⃣ Test the Website**

Open your CloudFront URL in the browser.

### **5️⃣ After Updating Files → Invalidate CloudFront Cache**

Example invalidation path:

```
/*
```

---

## 🧪 How to Run Locally

```bash
# Clone the repo
git clone https://github.com/FaustoSacco/aws-static-website-s3.git

cd aws-static-website-s3

# Open index.html in your browser
open index.html
```

---

## 📝 What I Learned

✔ How to host a static frontend on S3
✔ How S3 bucket policies work
✔ How CloudFront caches global content
✔ How to invalidate CloudFront cache after deployments
✔ How Git/GitHub versioning works for cloud projects
✔ How to structure a real AWS portfolio project

---

## 🏆 Why This Project Matters (Cloud Engineer POV)

This project demonstrates **real-world AWS skills**, including:

* Static hosting via S3
* CDN distribution with CloudFront
* Caching & invalidations (very important in interviews)
* Git version control
* Proper cloud project documentation





