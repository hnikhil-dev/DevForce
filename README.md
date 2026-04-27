<div align="center">
  <img src="https://img.shields.io/badge/GDG-Hackathon_Submission-blue?style=for-the-badge&logo=google" alt="GDG Hackathon" />
  <br><br>

  <h1>DevForce</h1>
  <p><b>Bridging the gap between code and collaboration.</b></p>
  
  > *"Because finding a technical partner should be as intuitive as writing a clean function."*
  
  <p>
    <img src="https://img.shields.io/badge/Flutter-02569B?style=flat-square&logo=flutter&logoColor=white" />
    <img src="https://img.shields.io/badge/Firebase-FFCA28?style=flat-square&logo=firebase&logoColor=black" />
    <img src="https://img.shields.io/badge/Dart-0175C2?style=flat-square&logo=dart&logoColor=white" />
    <img src="https://img.shields.io/badge/OpenStreetMap-7EBC6F?style=flat-square&logo=openstreetmap&logoColor=white" />
    <img src="https://img.shields.io/badge/Gemini_AI-8E75B2?style=flat-square&logo=google-gemini&logoColor=white" />
  </p>
</div>

---

## The Vision

Traditional networking platforms are often too formal or noisy, making it difficult to find the right people when time is of the essence. **DevForce** was created to solve the "find-a-teammate" friction during hackathons and technical sprints.

It is a proximity-aware networking platform designed to connect you with local developers in real-time. Whether you are looking for a designer to complement your backend skills or a peer-programming buddy in your current city, DevForce facilitates meaningful technical connections through a streamlined discovery interface.

---

## Technical Architecture

DevForce is built with a focus on performance, stability, and high-fidelity user experience.

### 1. High-Performance Proximity Mapping
We implemented a custom map engine utilizing **OpenStreetMap** to provide real-time location visualization without the overhead of proprietary mapping APIs.
* **Engineering Challenge:** Handling high-frequency coordinate updates and preventing rendering crashes during rapid zoom/pan gestures.
* **Solution:** Implemented a coordinate math sanitizer and strict camera boundary constraints to ensure 100% stability.

### 2. Real-Time Collaboration Hub
Communication is the core of any successful project. We engineered a low-latency messaging system powered by Firestore reactive streams.
* **Architecture:** To optimize performance, the application utilizes a lightweight background stream to monitor message state, allowing for instant badge updates and read status without heavy database polling.

### 3. Intelligence Layer (Gemini AI)
DevForce goes beyond simple profile matching. It utilizes **Google's Gemini 1.5 Flash** to analyze developer compatibility.
* **Smart Analysis:** The AI evaluates skill complementarity, experience levels, and shared hackathon interests to provide an "Compatibility Score."
* **Project Ideation:** Gemini suggests specific project ideas that match the combined strengths of two developers, providing an immediate starting point for hackathon teams.

---

## Design Philosophy

The UI is built from the ground up using a custom design system. We avoided generic component libraries to create a unique, premium aesthetic.
* **Glassmorphism:** Custom backdrop blur filters and layered transparency for a modern, depth-focused feel.
* **Motion Design:** An animated mesh background provides a dynamic atmosphere while maintaining a consistent 60fps on mobile and web.
* **Responsive Framework:** A single codebase delivers a native experience on Android and a fully responsive, desktop-optimized layout for the Web.

---

## For the Judges: Frictionless Testing

We value your time and made sure DevForce is pre-configured for immediate evaluation.

```bash
# 1. Clone the repository
git clone https://github.com/riteshamrutkar/DevForce.git

# 2. Install dependencies
cd DevForce
flutter pub get

# 3. Launch the application
flutter run
```

### The "Instant-Evaluation" Configuration
We have explicitly included the necessary Firebase configurations (`google-services.json` and web settings) within the repository. You do **not** need to perform any database setup or API key configuration. 

**Pro Tip:** Log in with two different Google accounts (one on Web, one on an Emulator) to witness the real-time proximity alerts and AI-driven match analysis work in unison.

---

<div align="center">
  Engineered with precision for the GDG community by <b>VectorFlow</b>.
</div>
