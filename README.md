# wellness_diary
Wellness Diary - Flutter App
A holistic health tracker for mood logging, medication reminders, and wellness insights

## 📱 App Overview  
Wellness Diary helps users:  
✔ Log daily moods with emoji + notes  
✔ Set smart medication reminders  
✔ Track health vitals (weight, blood pressure)  
✔ View AI-generated weekly insights  

Built with Flutter for cross-platform compatibility (iOS/Android).  

## ✨ Features  
-Feature	Implementation Details  
✔️Mood Tracking	Emoji selector + timestamped notes  
✔️Medication Alerts	Push notifications with Firebase Cloud Messaging  
✔️Health Dashboard	Charts (using charts_flutter) for trends  
✔️Form Validation	TextFormField validators for all inputs  
✔️Dark/Light Mode	Theme toggle with Provider state management  

## 🛠️ Technical Stack  
Frontend: Flutter (Dart)  

Backend: Firebase (Auth, Firestore, Cloud Functions)  

State Management: Provider  

Animations: Built-in Flutter (Hero, AnimatedContainer)  

Testing: flutter_test (Widget/Unit tests)  
## 🚀 Installation  
### 1.Clone the repo:  
bash  
git clone https://github.com/[yourusername]/wellness_diary.git  
cd wellness_diary  

### 2.Add Firebase Config:  
Place google-services.json (Android) in android/app/  
Place GoogleService-Info.plist (iOS) in ios/Runner/  

### 3.Install dependencies:  
bash  
flutter pub get  

### 4.Run the app:  
bash  
flutter run  

## 📂 Project Structure
lib/  
├── main.dart                  # Entry point  
├── models/                    # Data models  
│   ├── mood_entry.dart  
│   └── medication.dart  
├── screens/                   # UI Pages  
│   ├── home_screen.dart  
│   ├── mood_logger.dart  
│   └── reminders_screen.dart  
├── widgets/                   # Reusable components  
│   ├── custom_button.dart  
│   └── health_chart.dart  
├── services/                  # Business logic  
│   ├── auth_service.dart  
│   └── firestore_service.dart  
└── utils/                     # Helpers  
    ├── constants.dart         # Colors, padding  
    └── validators.dart        # Form validation  

## 🔧 Key Configurations  
Firebase Setup  
Enable Firestore (Test mode) and Authentication (Email/Password).  

Add security rules in firestore.rules:  

javascript  
rules_version = '2';  
service cloud.firestore {  
  match /databases/{database}/documents {  
    match /{document=**} {  
      allow read, write: if request.auth != null;   
    }  
  }  
}  

Environment Variables  
Create .env for sensitive keys:  
text  
FIREBASE_API_KEY=[your_key_here]    
Load using flutter_dotenv.  

## ✅ Testing  
Run widget tests:  
bash  
flutter test test/widget_test.dart  

## 📈 Future Roadmap  
Integrate Apple Health/Google Fit  

Add AI mood analysis (TensorFlow Lite)  

Multi-language support  

## 📜 License  
MIT © 2023 Fridah Lumadi  

Need Help?  
Open an issue or contact mathiasfridah2@gmail.com.  





A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.
