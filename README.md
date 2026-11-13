# FlowPilot_Agent
# 🤖 FlowPilot_Agent - AI-Powered Enterprise RPA Workflow

**FlowPilot_Agent** is an enterprise **UiPath Studio** RPA project leveraging the **Google Gemini API** for intelligent corporate policy analysis, automated conflict detection, and dynamic email routing.

---

## ⚙️ Configuration Guide (`Data/Config.xlsx`)

Before running the workflow on your local machine, you must configure the parameters located in **`Data/Config.xlsx`**.

> 💡 **Important:** Please review the **`Info`** column inside `Data/Config.xlsx`. It contains detailed descriptions and formatting instructions for every configuration parameter used in the project.

---

### 1. Obtaining a Gemini API Key (Google AI Studio)

To enable the AI analysis engine, generate a free API key from Google AI Studio:

1. Go to [Google AI Studio](https://aistudio.google.com/) and sign in with your Google account.
2. Click on **Get API key** in the left navigation bar.
3. Click **Create API key**, copy the generated key, and paste it into the corresponding API Key row in `Data/Config.xlsx`.

---

### 2. Generating a Gmail App Password (`EmailPassword`)

For the automated email notification workflow (`Send Mail`) to authenticate via Gmail SMTP, you must generate a 16-digit **Google App Password** rather than using your regular account password:

1. Navigate to your [Google Account Security Settings](https://myaccount.google.com/security).
2. Ensure that **2-Step Verification** is turned **ON**.
3. Use the top search bar to search for **App passwords** and open the settings page.
4. Enter an app name (e.g., `UiPath FlowPilot`) and click **Create**.
5. Copy the generated **16-character password** (without spaces) and paste it into the **`EmailPassword`** field inside `Data/Config.xlsx`.

---

## 📂 Project Structure

* **`Data/Config.xlsx`**: Central configuration file containing credentials, endpoints, and file paths (refer to the `Info` column for details).
* **`Data/Input/` & `Data/Archive/`**: Directories storing incoming corporate procedure documents (`.docx`) and archived files.
* **`ProcessWorkflows/`**: Modular `.xaml` workflows handling document parsing, AI API calls, and email dispatch.
* **`Main.xaml`**: Entry point of the automation process.

# 🤖 FlowPilot_Agent - AI Destekli Kurumsal RPA İş Akışı

**FlowPilot_Agent**, kurumsal prosedür ve politika dokümanlarını Google Gemini API kullanarak analiz eden, olası çelişkileri tespit eden ve sonuçları dinamik e-posta yönlendirmesiyle ilgili birimlere raporlayan bir **UiPath Studio** RPA projesidir.

---

## ⚙️ Kurulum ve Yapılandırma (`Data/Config.xlsx`)

Projeyi kendi ortamınızda çalıştırmadan önce **`Data/Config.xlsx`** dosyasını açarak gerekli parametreleri kendi bilgilerinizle doldurmanız gerekmektedir.

> 💡 **Önemli Not:** `Config.xlsx` dosyası içerisinde yer alan **`Info`** kolonunu mutlaka inceleyin. Her bir parametrenin ne işe yaradığı, hangi formatta girilmesi gerektiği ve iş akışında nerede kullanıldığı `Info` kolonunda detaylıca açıklanmıştır.

---

### 1. Google AI Studio'dan Gemini API Key Alma

Yapay zeka analizlerinin çalışabilmesi için kendi Gemini API anahtarınızı oluşturup `Config.xlsx` dosyasına eklemelisiniz:

1. [Google AI Studio](https://aistudio.google.com/) adresine gidin ve Google hesabınızla giriş yapın.
2. Sol menüde yer alan **Get API key** butonuna tıklayın.
3. **Create API key** seçeneğine basarak yeni bir API anahtarı oluşturun ve kopyalayın.
4. `Data/Config.xlsx` dosyasını açın ve ilgili API Key satırındaki `Value` hücresine anahtarınızı yapıştırın.

---

### 2. Gmail Uygulama Şifresi (App Password) Oluşturma (`EmailPassword`)

Sürecin sonunda otomatik e-posta gönderimi (`Send Mail`) yapılabilmesi için standart Gmail şifreniz **değil**, Google üzerinden alacağınız 16 haneli **Uygulama Şifresi (App Password)** kullanılmalıdır:

1. [Google Hesabım (My Account)](https://myaccount.google.com/) sayfasına gidin ve sol menüden **Güvenlik (Security)** sekmesine tıklayın.
2. "Google'da oturum açma" bölümünde **2 Adımlı Doğrulama (2-Step Verification)** özelliğinin **Açık** olduğundan emin olun *(kapalıysa önce aktif hale getirin)*.
3. Üstteki arama çubuğuna **Uygulama Şifreleri (App passwords)** yazın ve çıkan sonuca tıklayın.
4. Uygulama adı (App name) alanına `UiPath FlowPilot` yazın ve **Oluştur (Create)** butonuna tıklayın.
5. Ekranda beliren **16 haneli şifreyi** kopyalayın.
6. `Data/Config.xlsx` dosyasındaki **`EmailPassword`** satırının karşısına bu 16 haneli şifreyi (aradaki boşlukları silerek) yapıştırın.

---

## 📂 Proje Klasör Yapısı

* **`Data/Config.xlsx`**: Süreç parametreleri, dosya yolları, API ve e-posta ayarlarının tutulduğu ana yapılandırma dosyası (`Info` kolonundaki açıklamaları takip edin).
* **`Data/Input/` & `Data/Archive/`**: Analiz edilecek şirket prosedürlerinin (`.docx`) ve işlenmiş dosyaların tutulduğu klasörler.
* **`ProcessWorkflows/`**: Modüler `.xaml` iş akışı dosyaları.
* **`Main.xaml`**: Sürecin başlatıldığı ana iş akışı dosyası.

---

## 🚀 Çalıştırma

1. `Data/Config.xlsx` içindeki tüm zorunlu alanları (`Info` kolonunu referans alarak) doldurup dosyayı kaydedin ve kapatın.
2. Projeyi **UiPath Studio** ile açın.
3. Bağımlılıkların (Dependencies) yüklendiğinden emin olduktan sonra `Main.xaml` üzerinden projeyi **Run** (Çalıştır) diyerek başlatın.
