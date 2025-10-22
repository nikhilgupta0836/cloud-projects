
# 🌐 Host Your Static Website on **AWS S3**

Follow these simple steps to get your **HTML, CSS, JS** website live using **Amazon S3**. No servers required! 🚀

---

## **1️⃣ Create an S3 Bucket**

1. Go to **AWS Management Console → S3 → Create Bucket**.
2. Fill in the details:

   * **Bucket name:** Must be **globally unique** (e.g., `my-static-website-nikhil`)
   * **Region:** Choose your preferred region 🌍
   * **Uncheck** “Block all public access” ✅
3. Click **Create bucket** ➡️ Your bucket is ready!

---

## **2️⃣ Upload Your Website Files**

1. Open your bucket → **Upload → Add files / Add folder**.
2. Upload your website files:

   * `index.html` 📝
   * `style.css` 🎨
   * `script.js` ⚡
   * Images, fonts, or other assets 🖼️
3. Click **Upload** ➡️ Files are now in your bucket.

---

## **3️⃣ Enable Static Website Hosting**

1. Go to **Properties → Static website hosting → Enable**.
2. Configure:

   * **Index document:** `index.html` ✅
   * **Error document (optional):** `error.html` ❌
3. Click **Save**.
4. Copy the **Endpoint URL** → This is your **live website link** 🌐:

```
http://my-static-website-nikhil.s3-website-us-east-1.amazonaws.com
```

---

## **4️⃣ Make Your Website Public**

1. Go to **Permissions → Bucket Policy**.
2. Paste this JSON (replace `YOUR_BUCKET_NAME`):

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}
```

3. Click **Save** ✅
   Your website is now **publicly accessible**! 🎉

---

## **5️⃣ Optional: Use a Custom Domain & HTTPS**

* Link your bucket to a **custom domain** using **Route 53** or any DNS provider 🌐
* For **HTTPS**, use **CloudFront** in front of your S3 bucket 🔒

---

## **6️⃣ Summary**

| Step | Action                  | Emoji |
| ---- | ----------------------- | ----- |
| 1️⃣  | Create S3 bucket        | 🏗️   |
| 2️⃣  | Upload files            | 📂    |
| 3️⃣  | Enable static hosting   | ⚡     |
| 4️⃣  | Make public             | 🔓    |
| 5️⃣  | Optional domain & HTTPS | 🌐🔒  |

---

## **🎉 Your Website is Live!**

* No servers, no backend, only S3
* Publicly accessible via your **S3 website URL**
* Optional: custom domain + HTTPS 

---

inkn
Do you want me to do that next?
