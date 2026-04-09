# Instagram Brand Profiles Dataset

This dataset contains structured metadata for selected brands that are known for strong Instagram marketing performance. It provides detailed profile-level information and recent content activity for each account.

---

## 📁 Dataset Overview

Each JSON object represents a **single Instagram account** and includes:

- Profile metadata (username, bio, followers, etc.)
- Account classification (business/professional)
- Media statistics (posts, IGTV videos)
- Recent posts and IGTV content
- Related profiles

This dataset can be used for:

- Social media analytics
- Marketing research
- Influencer/brand benchmarking
- Machine learning applications (e.g., engagement prediction)

---

## 🧱 Data Structure

### 1\. Root Object

{\
 "requestMetadata": {...},\
 "id": "string",\
 "username": "string",\
 "fullName": "string",\
 ...\
}

---

## 🔑 Field Descriptions

### 📌 Request Metadata

| Field                    | Type         | Description               |
| ------------------------ | ------------ | ------------------------- |
| `requestMetadata.id`     | string       | Unique request identifier |
| `requestMetadata.status` | string       | API request status        |
| `requestMetadata.json`   | string (URL) | Link to raw JSON data     |

---

### 👤 Profile Information

| Field              | Type    | Description                      |
| ------------------ | ------- | -------------------------------- |
| `id`               | string  | Instagram user ID                |
| `username`         | string  | Instagram handle                 |
| `fullName`         | string  | Display name                     |
| `biography`        | string  | Profile bio                      |
| `businessCategory` | string  | Business category (if available) |
| `bioLinks`         | array   | Links in bio                     |
| `externalUrls`     | string  | External URL                     |
| `verified`         | boolean | Verified account status          |

---

### 📊 Account Metrics

| Field             | Type   | Description                 |
| ----------------- | ------ | --------------------------- |
| `followersCount`  | number | Number of followers         |
| `followsCount`    | number | Number of accounts followed |
| `postsCount`      | number | Total posts                 |
| `igtvVideoCount`  | number | Number of IGTV videos       |
| `highlightsCount` | number | Story highlights count      |

---

### 🏢 Account Type

| Field                   | Type    | Description               |
| ----------------------- | ------- | ------------------------- |
| `isBusinessAccount`     | boolean | Business account flag     |
| `isProfessionalAccount` | boolean | Professional account flag |

---

### 🖼️ Profile Images

| Field             | Type   | Description                       |
| ----------------- | ------ | --------------------------------- |
| `profilePicUrl`   | string | Profile picture (low resolution)  |
| `profilePicUrlHD` | string | Profile picture (high resolution) |

---

### 🎥 Latest IGTV Videos

Array: `latestIgtvVideos`

Each object includes:

| Field           | Description         |
| --------------- | ------------------- |
| `id`            | Media ID            |
| `shortcode`     | Instagram shortcode |
| `caption`       | Post caption        |
| `type`          | Media type (Video)  |
| `url`           | Post URL            |
| `likesCount`    | Number of likes     |
| `commentsCount` | Number of comments  |
| `timestamp`     | ISO timestamp       |
| `mentions`      | Tagged users        |
| `images`        | Thumbnail images    |

---

### 📸 Latest Posts

Array: `latestPosts`

Supports multiple content types:

- `Image`
- `Video`
- `Carousel`

Each post includes:

| Field           | Description         |
| --------------- | ------------------- |
| `id`            | Post ID             |
| `shortcode`     | Instagram shortcode |
| `caption`       | Post caption        |
| `type`          | Content type        |
| `hashtags`      | Extracted hashtags  |
| `mentions`      | Tagged users        |
| `likesCount`    | Number of likes     |
| `commentsCount` | Number of comments  |
| `timestamp`     | ISO timestamp       |
| `displayUrl`    | Main media URL      |
| `images`        | Media variants      |
| `taggedUsers`   | Tagged accounts     |

---

### 🔗 Related Profiles

Array: `relatedProfiles`

| Field           | Description         |
| --------------- | ------------------- |
| `id`            | Profile ID          |
| `username`      | Instagram handle    |
| `fullName`      | Display name        |
| `isVerified`    | Verification status |
| `profilePicUrl` | Profile image       |
