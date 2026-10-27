# Chinese Story Performance Project · Key Stage 2

An interactive, responsive web-based library of classic stories and Chinese legends, adapted into simple Chinese performance scripts for primary school children (Key Stage 2). 

## 📖 About the Project

This project turns familiar stories (from English lessons, storytime, and traditional tales) into actable Mandarin scripts. Each story is broken down into simple scenes with short, repetitive lines that are easy for young learners to memorize and perform.

### Key Features:
*   **Pinyin & English Support:** Every Chinese sentence features Pinyin directly above the characters (using ruby text) and the English translation below, making it accessible for non-Mandarin speaking adults and children.
*   **Audio Pronunciation:** Includes a built-in text-to-speech feature. Click the 🔊 icon next to any sentence to hear it read aloud in Mandarin. Click again to pause, and again to resume.
*   **Play Scene:** A "Play Scene" button allows children to listen to a whole scene at once.
*   **Print-Ready Scripts:** A dedicated "Print / Save as PDF" button on every story automatically formats the page into a clean, distraction-free rehearsal script. The printout includes a QR code linking back to the website for home practice.
*   **Responsive Design:** Fully responsive layout that works beautifully on laptops, tablets, and mobile phones.
*   **Organized Categories:** Stories are grouped into three themes:
    1.  Cross-Curricular & Social Themes
    2.  Classic Picture Books & Fairy Tales
    3.  Chinese Legends, Idioms & Folktales

## 🚀 How to Use

1.  **In the Classroom:** Open the `index.html` file in any web browser. Click on a story to view the script. Use the "Play Scene" or individual 🔊 buttons to practise pronunciation with the class. 
2.  **For Rehearsals:** Click the "Print / Save as PDF" button to generate a physical copy of the script for the children to hold and act out. 
3.  **At Home:** Children or parents can scan the QR code printed on the scripts (or on the website header) to access the site from a home device, allowing them to practise the audio at home.

## 🌐 How to Host on GitHub Pages

If you are updating the site or moving it to a new repository, follow these steps to make it live:

1.  Upload the `index.html` file (and this `README.md` file) to your GitHub repository.
2.  Go to the **Settings** tab of your repository.
3.  On the left sidebar, click **Pages**.
4.  Under the "Build and deployment" section, set the Source to **Deploy from a branch**.
5.  Under "Branch", select **main** (or `master`) and the `/ (root)` folder, then click **Save**.
6.  Wait a minute or two. Your site will be published at `https://[your-username].github.io/[your-repo-name]/`.

### ⚠️ Important: Updating the QR Code
Before sharing the link, you must update the QR code in the code so it points to your live website. 
1. Open `index.html` in a text editor (like VS Code).
2. Scroll to the bottom and look for `const siteUrl = "https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/";` (around line 1550).
3. Replace the placeholder text with your actual GitHub Pages URL. The QR codes on the screen and on the printed PDFs will automatically update.

## 🛠 How to Add New Stories

The website is built as a **single, self-contained HTML file**. This makes it easy to host, but it means you have to edit the HTML directly to add a new story. 

1.  **Add the Story Card:** In the `<section class="panel" id="cat1">` (or `cat2`/`cat3`), copy an existing `<div class="card">` block and paste it where you want the new story to appear. Update the image URL, Pinyin, Chinese title, and English title.
2.  **Create the Story Panel:** Scroll down to the other story panels (e.g., `<section class="panel" id="billy">`). Copy an entire `<section>` block and paste it at the bottom of the other stories. 
3.  **Update IDs:** Change the `id` of the new section to match your new story (e.g., `id="new_story"`). Update the `data-goto` attribute on your new Card to match this ID.
4.  **Add the Scenes and Lines:** Inside your new section, copy the `<div class="line">` blocks. Update the `data-audio` attribute (plain text for the voice generator), the `<div class="cn">` (with ruby tags for Pinyin), and the `<div class="en">` text.
5.  **Update the `show()` function:** Scroll to the bottom of the file, find the JavaScript `show(id)` function, and add your new story ID to the correct category array (e.g., add `'new_story'` to the `cat1` array).

## 📚 Story List

*   **Cross-Curricular & Social Themes:**
    *   Billy's Beetle (比利的甲壳虫)
    *   Paddington Visits London (帕丁顿游览伦敦)
    *   Jim and the Beanstalk (杰姆与仙豆)
    *   Lost and Found (迷失与找到)
    *   The Journey Home (回家之旅)
    *   Flower Block (开花大楼)
*   **Classic Picture Books & Fairy Tales:**
    *   Elmer the Patchwork Elephant (花格子大象艾玛)
    *   The Very Hungry Caterpillar (好饿的毛毛虫)
    *   The Gruffalo (咕噜牛)
    *   The Tiger Who Came to Tea (老虎来喝下午茶)
    *   The Colour Monster (情绪小怪兽)
    *   Little Red Riding Hood (小红帽)
    *   The Mixed-Up Chameleon (拼拼凑凑的变色龙)
    *   Charlotte's Web (夏洛的网)
    *   Matilda (玛蒂尔达)
    *   Alice in Wonderland (爱丽丝梦游仙境)
    *   Frozen (冰雪奇缘)
*   **Chinese Legends, Idioms & Folktales:**
    *   The Enormous Turnip (拔萝卜)
    *   The Tortoise and the Hare (龟兔赛跑)
    *   The Moon in the Well (猴子捞月)
    *   The Clever Fox (狐假虎威)
    *   Kong Rong and the Pears (孔融让梨)
    *   Little Nian (小年兽)
    *   Little Tadpoles Look for Mummy (小蝌蚪找妈妈)
    *   Journey to the West: The Birth of the Stone Monkey (石猴出世)
    *   Journey to the West: Three Defeats of the White Bone Demon (三打白骨精)
    *   Journey to the West: Three Attempts to Borrow the Banana Fan (三借芭蕉扇)
