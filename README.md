https://lovable.dev/preview/ukTry32zn0VEHu2B0vhtaveKuqmNFGgi

import { createFileRoute } from "@tanstack/react-router";
import { motion } from "framer-motion";
import {
  Download,
  Mail,
  Github,
  Linkedin,
  ArrowRight,
  Code2,
  Brain,
  Wrench,
  Sparkles,
  Users,
  MessageSquare,
  Lightbulb,
  Clock,
  Zap,
  Heart,
  Award,
  ExternalLink,
  FileText,
  Trophy,
  GraduationCap,
  Calendar,
  Rocket,
  Send,
  MapPin,
  CheckCircle2,
} from "lucide-react";
import { useState } from "react";
import { Nav } from "@/components/portfolio/Nav";
import { Particles } from "@/components/portfolio/Particles";
import { Typewriter } from "@/components/portfolio/Typewriter";
import { Counter } from "@/components/portfolio/Counter";

export const Route = createFileRoute("/")({
  component: Portfolio,
});

const fadeUp = {
  initial: { opacity: 0, y: 30 },
  whileInView: { opacity: 1, y: 0 },
  viewport: { once: true, margin: "-80px" },
  transition: { duration: 0.6, ease: [0.2, 0.8, 0.2, 1] as const },
};

const skillGroups = [
  {
    icon: Code2,
    title: "Programming",
    items: ["Python", "SQL"],
  },
  {
    icon: Brain,
    title: "AI & Machine Learning",
    items: [
      "ML Fundamentals",
      "Data Preprocessing",
      "Model Training",
      "Scikit-learn",
      "Pandas",
      "NumPy",
    ],
  },
  {
    icon: Wrench,
    title: "Tools",
    items: ["Git", "GitHub", "Jupyter", "VS Code"],
  },
  {
    icon: Sparkles,
    title: "Soft Skills",
    items: [
      "Leadership",
      "Team Collaboration",
      "Problem Solving",
      "Communication",
      "Critical Thinking",
      "Time Management",
      "Adaptability",
      "Mentoring",
    ],
  },
];

const leadership = [
  { icon: Users, title: "Team Leadership", text: "Guides classmates through academic activities and coordinates collaborative work." },
  { icon: Lightbulb, title: "Peer Mentoring", text: "Helps peers understand programming and AI concepts with patience and clarity." },
  { icon: Heart, title: "Supportive Attitude", text: "Assists teammates in completing projects, assignments, and technical challenges." },
  { icon: MessageSquare, title: "Clear Communication", text: "Bridges ideas across teams with strong verbal and written communication." },
  { icon: Zap, title: "Continuous Growth", text: "Believes in lifelong learning, iteration, and sharing knowledge openly." },
  { icon: Clock, title: "Reliable Delivery", text: "Manages time well and shows up prepared for team commitments." },
];

const certifications = [
  {
    name: "Honeywell Certificate",
    org: "Honeywell",
    date: "2024",
  },
  {
    name: "Python Programming Certificate",
    org: "Certified Program",
    date: "2024",
  },
];

const projects = [
  {
    title: "AI Study Assistant",
    desc: "A Python app that uses LLM APIs to summarize notes, generate quizzes, and answer subject questions for students.",
    tech: ["Python", "OpenAI API", "Streamlit"],
    features: ["Note summarization", "Auto quiz generation", "Chat-style Q&A"],
  },
  {
    title: "Fake News Detector",
    desc: "An AI-powered web tool that classifies news articles as real or fake using NLP and classical ML.",
    tech: ["Python", "NLTK", "Scikit-learn"],
    features: ["TF-IDF pipeline", "Logistic Regression model", "Simple web UI"],
  },
  {
    title: "Movie Recommender App",
    desc: "Content-based recommendation app that suggests movies from a user's taste profile using cosine similarity.",
    tech: ["Python", "Pandas", "Streamlit"],
    features: ["Content-based filtering", "Interactive UI", "Top-N results"],
  },
  {
    title: "Spam Email Classifier",
    desc: "A lightweight AI tool that filters spam messages with high precision using Naive Bayes.",
    tech: ["Python", "NLTK", "Scikit-learn"],
    features: ["Text cleaning", "Naive Bayes model", "Precision tuning"],
  },
  {
    title: "Handwritten Digit Recognizer",
    desc: "Interactive app that recognizes hand-drawn digits in real time using an MNIST-trained model.",
    tech: ["Python", "NumPy", "Scikit-learn"],
    features: ["Canvas input", "MNIST-trained model", "> 95% accuracy"],
  },
  {
    title: "Student Performance Predictor",
    desc: "Predicts student outcomes from study habits and demographics — helpful for early academic support.",
    tech: ["Python", "Scikit-learn", "Pandas"],
    features: ["EDA & features", "Model comparison", "Insights dashboard"],
  },
];

const achievements = [
  { icon: Award, title: "Honeywell Certification", date: "2024", text: "Earned recognized certification through Honeywell program." },
  { icon: Award, title: "Python Certification", date: "2024", text: "Completed structured Python programming certification." },
  { icon: Users, title: "Leadership Activities", date: "Ongoing", text: "Led academic team activities and peer study groups." },
  { icon: GraduationCap, title: "Academic Milestones", date: "2023–2026", text: "Consistent progress across Diploma AI & ML curriculum." },
  { icon: Lightbulb, title: "Workshops", date: "Ongoing", text: "Participated in AI/ML workshops and technical sessions." },
  { icon: Rocket, title: "Technical Events", date: "Ongoing", text: "Active in departmental technical events and demos." },
  { icon: Trophy, title: "Hackathons", date: "Upcoming", text: "Preparing to compete in inter-college hackathons." },
  { icon: Brain, title: "AI Competitions", date: "Upcoming", text: "Targeting Kaggle and campus AI competitions." },
];

function Portfolio() {
  return (
    <div id="top" className="relative">
      <Nav />
      <main>
        <Hero />
        <About />
        <Skills />
        <Leadership />
        <Certifications />
        <Projects />
        <Achievements />
        <Resume />
        <Contact />
      </main>
      <Footer />
    </div>
  );
}

function Hero() {
  return (
    <section className="relative min-h-dvh flex items-center overflow-hidden pt-24 pb-16">
      <Particles />
      <div className="absolute top-1/4 -left-20 w-96 h-96 rounded-full bg-primary/20 blur-3xl animate-float" aria-hidden />
      <div className="absolute bottom-1/4 -right-20 w-96 h-96 rounded-full bg-accent/20 blur-3xl animate-float" style={{ animationDelay: "2s" }} aria-hidden />

      <div className="relative mx-auto max-w-7xl px-6 w-full grid lg:grid-cols-[1.4fr_1fr] gap-12 items-center">
        <div>
          <motion.p
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6 }}
            className="inline-flex items-center gap-2 glass rounded-full px-4 py-1.5 text-xs font-medium text-muted-foreground mb-6"
          >
            <span className="w-2 h-2 rounded-full bg-accent animate-pulse" />
            Available for Internships
          </motion.p>

          <motion.h1
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.7, delay: 0.1 }}
            className="text-5xl sm:text-6xl lg:text-7xl font-bold leading-[1.05] tracking-tight"
          >
            Hi, I'm <span className="text-gradient">Sravani Kallemolam</span>
          </motion.h1>

          <motion.div
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6, delay: 0.25 }}
            className="mt-6 text-xl sm:text-2xl text-muted-foreground font-medium min-h-[2.2em]"
          >
            <Typewriter
              words={[
                "AI & Machine Learning Student",
                "Building AI-powered apps with Python",
                "Aspiring AI Developer",
              ]}
            />
          </motion.div>

          <motion.p
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6, delay: 0.4 }}
            className="mt-6 text-base sm:text-lg text-muted-foreground max-w-2xl leading-relaxed"
          >
            Curious about AI tools, passionate about Python, and always learning.
            I build practical AI applications that solve real problems — and I love
            helping teammates level up along the way.
          </motion.p>

          <motion.div
            initial={{ opacity: 0, y: 20 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6, delay: 0.55 }}
            className="mt-10 flex flex-wrap gap-3"
          >
            <a
              href="#projects"
              className="group inline-flex items-center gap-2 px-6 py-3 rounded-full bg-gradient-primary text-primary-foreground font-semibold shadow-glow hover:scale-105 transition-transform"
            >
              View Projects
              <ArrowRight size={18} className="group-hover:translate-x-1 transition-transform" />
            </a>
            <a
              href="/resume.pdf"
              download
              className="inline-flex items-center gap-2 px-6 py-3 rounded-full glass hover:border-primary/50 border border-border font-semibold transition-colors"
            >
              <Download size={18} />
              Download Resume
            </a>
            <a
              href="#contact"
              className="inline-flex items-center gap-2 px-6 py-3 rounded-full glass hover:border-primary/50 border border-border font-semibold transition-colors"
            >
              <Mail size={18} />
              Contact Me
            </a>
          </motion.div>

          <motion.div
            initial={{ opacity: 0 }}
            animate={{ opacity: 1 }}
            transition={{ duration: 0.8, delay: 0.8 }}
            className="mt-14 grid grid-cols-3 gap-6 max-w-md"
          >
            {[
              { n: 6, s: "+", label: "Projects" },
              { n: 2, s: "+", label: "Certifications" },
              { n: 3, s: "rd", label: "Year Diploma" },
            ].map((s) => (
              <div key={s.label}>
                <div className="text-3xl font-bold text-gradient">
                  <Counter value={s.n} suffix={s.s} />
                </div>
                <div className="text-xs text-muted-foreground mt-1">{s.label}</div>
              </div>
            ))}
          </motion.div>
        </div>

        <motion.div
          initial={{ opacity: 0, scale: 0.9 }}
          animate={{ opacity: 1, scale: 1 }}
          transition={{ duration: 0.8, delay: 0.3 }}
          className="hidden lg:block"
        >
          <HeroOrb />
        </motion.div>
      </div>
    </section>
  );
}

function HeroOrb() {
  return (
    <div className="relative aspect-square max-w-md mx-auto">
      <div className="absolute inset-0 rounded-full bg-gradient-primary blur-3xl opacity-40 animate-float" />
      <div className="relative aspect-square rounded-full glass-strong border border-primary/30 flex items-center justify-center overflow-hidden">
        <div className="absolute inset-4 rounded-full border border-primary/20" />
        <div className="absolute inset-10 rounded-full border border-accent/20" />
        <div className="absolute inset-16 rounded-full border border-purple/20" />
        <div className="relative z-10 text-center">
          <Brain size={80} className="mx-auto text-primary mb-3" strokeWidth={1.3} />
          <div className="font-display font-bold text-2xl text-gradient">AI · ML</div>
          <div className="text-xs text-muted-foreground mt-1 tracking-widest uppercase">Engineer in Training</div>
        </div>
        {[0, 60, 120, 180, 240, 300].map((deg, i) => (
          <div
            key={i}
            className="absolute w-2 h-2 rounded-full bg-primary shadow-glow"
            style={{
              top: "50%",
              left: "50%",
              transform: `rotate(${deg}deg) translate(160px) rotate(-${deg}deg)`,
              animation: `float 4s ease-in-out ${i * 0.3}s infinite`,
            }}
          />
        ))}
      </div>
    </div>
  );
}

function SectionHeader({ eyebrow, title, sub }: { eyebrow: string; title: string; sub?: string }) {
  return (
    <motion.div {...fadeUp} className="max-w-3xl mb-14">
      <div className="inline-flex items-center gap-2 glass rounded-full px-3 py-1 text-xs font-medium text-primary mb-4">
        <span className="w-1.5 h-1.5 rounded-full bg-primary" />
        {eyebrow}
      </div>
      <h2 className="text-4xl sm:text-5xl font-bold tracking-tight">
        {title.split("·").map((part, i, arr) => (
          <span key={i}>
            {i === arr.length - 1 && arr.length > 1 ? <span className="text-gradient">{part}</span> : part}
            {i < arr.length - 1 && " · "}
          </span>
        ))}
      </h2>
      {sub && <p className="mt-4 text-lg text-muted-foreground leading-relaxed">{sub}</p>}
    </motion.div>
  );
}

function About() {
  return (
    <section id="about" className="relative py-24 px-6">
      <div className="mx-auto max-w-7xl">
        <SectionHeader eyebrow="About" title="About · Me" />
        <div className="grid lg:grid-cols-[1fr_1.3fr] gap-10">
          <motion.div {...fadeUp} className="glass rounded-2xl p-8 card-hover">
            <GraduationCap className="text-primary mb-4" size={32} />
            <h3 className="text-xl font-semibold mb-2">Education</h3>
            <p className="text-muted-foreground text-sm leading-relaxed">
              Diploma — 3rd Year<br />
              Artificial Intelligence & Machine Learning
            </p>
            <div className="mt-6 pt-6 border-t border-border">
              <div className="text-xs uppercase tracking-widest text-muted-foreground mb-2">Career Goal</div>
              <p className="text-sm leading-relaxed">
                Become an <span className="text-foreground font-medium">AI Developer</span> who ships useful, human-friendly AI applications and keeps growing every day.
              </p>
            </div>
          </motion.div>

          <motion.div {...fadeUp} className="space-y-5">
            <p className="text-lg leading-relaxed text-muted-foreground">
              I'm a <span className="text-foreground font-medium">Diploma 3rd Year student</span> in AI & Machine Learning, endlessly curious about new AI tools and how to bend them into real applications. I love turning ideas into working Python projects — from chat assistants to classifiers — and learning something new with every build.
            </p>
            <p className="text-lg leading-relaxed text-muted-foreground">
              Beyond code, I enjoy <span className="text-foreground font-medium">helping classmates</span> understand tricky concepts, leading team projects, and keeping the collaboration vibe strong. I believe the best engineers grow together.
            </p>
            <p className="text-lg leading-relaxed text-muted-foreground">
              Right now I'm looking for an <span className="text-foreground font-medium">internship</span> where I can contribute to real AI products, learn from experienced engineers, and keep sharpening my craft.
            </p>
          </motion.div>
        </div>
      </div>
    </section>
  );
}

function Skills() {
  return (
    <section id="skills" className="relative py-24 px-6">
      <div className="mx-auto max-w-7xl">
        <SectionHeader
          eyebrow="Skills"
          title="Tech · Stack"
          sub="A growing toolkit spanning programming, machine learning, developer tools, and the human skills that make teams thrive."
        />
        <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-5">
          {skillGroups.map((group, i) => (
            <motion.div
              key={group.title}
              initial={{ opacity: 0, y: 30 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true, margin: "-50px" }}
              transition={{ duration: 0.5, delay: i * 0.08 }}
              className="glass rounded-2xl p-6 card-hover group"
            >
              <div className="w-12 h-12 rounded-xl bg-gradient-primary/20 flex items-center justify-center mb-4 group-hover:scale-110 transition-transform">
                <group.icon className="text-primary" size={22} />
              </div>
              <h3 className="font-semibold text-lg mb-4">{group.title}</h3>
              <ul className="flex flex-wrap gap-2">
                {group.items.map((it) => (
                  <li
                    key={it}
                    className="text-xs px-3 py-1.5 rounded-full bg-secondary/60 border border-border text-muted-foreground hover:text-foreground hover:border-primary/50 transition-colors"
                  >
                    {it}
                  </li>
                ))}
              </ul>
            </motion.div>
          ))}
        </div>
      </div>
    </section>
  );
}

function Leadership() {
  return (
    <section id="leadership" className="relative py-24 px-6">
      <div className="mx-auto max-w-7xl">
        <SectionHeader
          eyebrow="Community"
          title="Leadership & Community · Impact"
          sub="Great technology is built through teamwork, communication, and a willingness to help others succeed."
        />
        <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-5">
          {leadership.map((l, i) => (
            <motion.div
              key={l.title}
              initial={{ opacity: 0, y: 30 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true, margin: "-50px" }}
              transition={{ duration: 0.5, delay: i * 0.06 }}
              className="glass rounded-2xl p-6 card-hover"
            >
              <div className="w-11 h-11 rounded-xl bg-gradient-primary/20 flex items-center justify-center mb-4">
                <l.icon className="text-accent" size={20} />
              </div>
              <h3 className="font-semibold mb-2">{l.title}</h3>
              <p className="text-sm text-muted-foreground leading-relaxed">{l.text}</p>
            </motion.div>
          ))}
        </div>
      </div>
    </section>
  );
}

function Certifications() {
  return (
    <section id="certifications" className="relative py-24 px-6">
      <div className="mx-auto max-w-7xl">
        <SectionHeader eyebrow="Credentials" title="Certifications" />
        <div className="grid md:grid-cols-2 gap-5">
          {certifications.map((c, i) => (
            <motion.div
              key={c.name}
              initial={{ opacity: 0, y: 30 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true }}
              transition={{ duration: 0.5, delay: i * 0.1 }}
              className="glass rounded-2xl p-7 card-hover"
            >
              <div className="flex items-start justify-between mb-5">
                <div className="w-14 h-14 rounded-xl bg-gradient-primary/20 flex items-center justify-center">
                  <Award className="text-primary" size={26} />
                </div>
                <span className="text-xs text-muted-foreground glass rounded-full px-3 py-1">{c.date}</span>
              </div>
              <h3 className="text-xl font-semibold mb-1">{c.name}</h3>
              <p className="text-sm text-muted-foreground mb-6">{c.org}</p>
              <div className="flex gap-2">
                <button className="inline-flex items-center gap-1.5 text-xs px-3 py-2 rounded-lg bg-gradient-primary text-primary-foreground font-medium hover:scale-105 transition-transform">
                  <ExternalLink size={14} /> View
                </button>
                <button className="inline-flex items-center gap-1.5 text-xs px-3 py-2 rounded-lg glass border border-border hover:border-primary/50 font-medium transition-colors">
                  <Download size={14} /> Download
                </button>
              </div>
            </motion.div>
          ))}
        </div>
      </div>
    </section>
  );
}

function Projects() {
  return (
    <section id="projects" className="relative py-24 px-6">
      <div className="mx-auto max-w-7xl">
        <SectionHeader
          eyebrow="Work"
          title="Featured · Projects"
          sub="Applied machine learning projects that translate real datasets into working models."
        />
        <div className="grid md:grid-cols-2 lg:grid-cols-3 gap-5">
          {projects.map((p, i) => (
            <motion.article
              key={p.title}
              initial={{ opacity: 0, y: 30 }}
              whileInView={{ opacity: 1, y: 0 }}
              viewport={{ once: true, margin: "-50px" }}
              transition={{ duration: 0.5, delay: (i % 3) * 0.08 }}
              className="glass rounded-2xl overflow-hidden card-hover flex flex-col"
            >
              <div className="relative aspect-[16/10] bg-gradient-primary/30 overflow-hidden border-b border-border">
                <div className="absolute inset-0 flex items-center justify-center">
                  <Brain className="text-primary/40" size={80} strokeWidth={1} />
                </div>
                <div className="absolute inset-0 bg-gradient-to-t from-background/80 to-transparent" />
                <div className="absolute bottom-3 left-4 text-xs uppercase tracking-widest text-muted-foreground">
                  Project 0{i + 1}
                </div>
              </div>
              <div className="p-6 flex-1 flex flex-col">
                <h3 className="font-semibold text-lg mb-2">{p.title}</h3>
                <p className="text-sm text-muted-foreground leading-relaxed mb-4">{p.desc}</p>
                <ul className="space-y-1.5 mb-5">
                  {p.features.map((f) => (
                    <li key={f} className="flex items-start gap-2 text-xs text-muted-foreground">
                      <CheckCircle2 size={14} className="text-accent shrink-0 mt-0.5" />
                      {f}
                    </li>
                  ))}
                </ul>
                <div className="flex flex-wrap gap-1.5 mb-5">
                  {p.tech.map((t) => (
                    <span
                      key={t}
                      className="text-[10px] px-2 py-1 rounded-md bg-secondary/60 border border-border text-muted-foreground uppercase tracking-wider"
                    >
                      {t}
                    </span>
                  ))}
                </div>
                <div className="flex gap-2 mt-auto pt-3 border-t border-border">
                  <a
                    href="#"
                    className="flex-1 inline-flex items-center justify-center gap-1.5 text-xs px-3 py-2 rounded-lg glass border border-border hover:border-primary/50 transition-colors"
                  >
                    <Github size={14} /> Code
                  </a>
                  <a
                    href="#"
                    className="flex-1 inline-flex items-center justify-center gap-1.5 text-xs px-3 py-2 rounded-lg bg-gradient-primary text-primary-foreground font-medium hover:scale-105 transition-transform"
                  >
                    <ExternalLink size={14} /> Demo
                  </a>
                </div>
              </div>
            </motion.article>
          ))}
        </div>
      </div>
    </section>
  );
}

function Achievements() {
  return (
    <section id="achievements" className="relative py-24 px-6">
      <div className="mx-auto max-w-5xl">
        <SectionHeader eyebrow="Journey" title="Achievements · Timeline" />
        <div className="relative">
          <div className="absolute left-4 md:left-1/2 top-0 bottom-0 w-px bg-gradient-to-b from-primary/60 via-accent/40 to-transparent" />
          <div className="space-y-6">
            {achievements.map((a, i) => (
              <motion.div
                key={a.title}
                initial={{ opacity: 0, x: i % 2 === 0 ? -30 : 30 }}
                whileInView={{ opacity: 1, x: 0 }}
                viewport={{ once: true, margin: "-30px" }}
                transition={{ duration: 0.5 }}
                className={`relative flex items-start gap-5 md:gap-0 md:grid md:grid-cols-2 ${
                  i % 2 === 0 ? "" : "md:flex-row-reverse"
                }`}
              >
                <div className={`hidden md:block ${i % 2 === 0 ? "md:pr-12 md:text-right" : "md:col-start-2 md:pl-12"}`}>
                  <TimelineCard a={a} />
                </div>
                <div className="absolute left-4 md:left-1/2 -translate-x-1/2 w-3 h-3 rounded-full bg-gradient-primary shadow-glow ring-4 ring-background mt-6" />
                <div className="pl-12 md:hidden">
                  <TimelineCard a={a} />
                </div>
              </motion.div>
            ))}
          </div>
        </div>
      </div>
    </section>
  );
}

function TimelineCard({ a }: { a: (typeof achievements)[number] }) {
  return (
    <div className="glass rounded-xl p-5 card-hover inline-block text-left">
      <div className="flex items-center gap-3 mb-2">
        <div className="w-9 h-9 rounded-lg bg-gradient-primary/20 flex items-center justify-center">
          <a.icon className="text-primary" size={16} />
        </div>
        <div className="inline-flex items-center gap-1 text-xs text-muted-foreground">
          <Calendar size={12} /> {a.date}
        </div>
      </div>
      <h3 className="font-semibold mb-1">{a.title}</h3>
      <p className="text-sm text-muted-foreground leading-relaxed">{a.text}</p>
    </div>
  );
}

function Resume() {
  return (
    <section id="resume" className="relative py-24 px-6">
      <div className="mx-auto max-w-4xl">
        <motion.div
          {...fadeUp}
          className="glass-strong rounded-3xl p-10 sm:p-14 text-center relative overflow-hidden"
        >
          <div className="absolute -top-20 -right-20 w-64 h-64 rounded-full bg-primary/20 blur-3xl" />
          <div className="absolute -bottom-20 -left-20 w-64 h-64 rounded-full bg-accent/20 blur-3xl" />
          <div className="relative">
            <FileText className="mx-auto text-primary mb-4" size={40} />
            <h2 className="text-3xl sm:text-4xl font-bold mb-3">
              My <span className="text-gradient">Resume</span>
            </h2>
            <p className="text-muted-foreground max-w-xl mx-auto mb-8">
              A concise snapshot of my education, projects, certifications, and skills.
            </p>
            <div className="flex flex-wrap justify-center gap-3">
              <a
                href="/resume.pdf"
                target="_blank"
                rel="noreferrer"
                className="inline-flex items-center gap-2 px-6 py-3 rounded-full bg-gradient-primary text-primary-foreground font-semibold shadow-glow hover:scale-105 transition-transform"
              >
                <ExternalLink size={18} /> View Resume
              </a>
              <a
                href="/resume.pdf"
                download
                className="inline-flex items-center gap-2 px-6 py-3 rounded-full glass border border-border hover:border-primary/50 font-semibold transition-colors"
              >
                <Download size={18} /> Download Resume
              </a>
            </div>
          </div>
        </motion.div>
      </div>
    </section>
  );
}

function Contact() {
  const [form, setForm] = useState({ name: "", email: "", subject: "", message: "" });
  const [sent, setSent] = useState(false);

  const onSubmit = (e: React.FormEvent) => {
    e.preventDefault();
    const body = encodeURIComponent(`${form.message}\n\nFrom: ${form.name} <${form.email}>`);
    const subject = encodeURIComponent(form.subject || "Portfolio inquiry");
    window.location.href = `mailto:sravani@example.com?subject=${subject}&body=${body}`;
    setSent(true);
  };

  return (
    <section id="contact" className="relative py-24 px-6">
      <div className="mx-auto max-w-6xl">
        <SectionHeader
          eyebrow="Contact"
          title="Let's · Connect"
          sub="I'm actively looking for AI/ML internship opportunities and collaborations."
        />
        <div className="grid lg:grid-cols-[1fr_1.3fr] gap-8">
          <motion.div {...fadeUp} className="space-y-4">
            <div className="glass rounded-2xl p-6 card-hover">
              <Mail className="text-primary mb-3" size={22} />
              <div className="text-xs uppercase tracking-widest text-muted-foreground mb-1">Email</div>
              <a href="mailto:sravani@example.com" className="text-sm font-medium hover:text-primary transition-colors break-all">
                sravani@example.com
              </a>
            </div>
            <div className="glass rounded-2xl p-6 card-hover">
              <MapPin className="text-primary mb-3" size={22} />
              <div className="text-xs uppercase tracking-widest text-muted-foreground mb-1">Location</div>
              <div className="text-sm font-medium">India · Remote friendly</div>
            </div>
            <div className="glass rounded-2xl p-6">
              <div className="text-xs uppercase tracking-widest text-muted-foreground mb-3">Social</div>
              <div className="flex gap-2">
                {[
                  { icon: Github, href: "#", label: "GitHub" },
                  { icon: Linkedin, href: "#", label: "LinkedIn" },
                  { icon: Mail, href: "mailto:sravani@example.com", label: "Email" },
                ].map((s) => (
                  <a
                    key={s.label}
                    href={s.href}
                    aria-label={s.label}
                    className="w-11 h-11 rounded-xl glass border border-border flex items-center justify-center hover:border-primary/50 hover:text-primary transition-colors"
                  >
                    <s.icon size={18} />
                  </a>
                ))}
              </div>
            </div>
          </motion.div>

          <motion.form
            {...fadeUp}
            onSubmit={onSubmit}
            className="glass-strong rounded-2xl p-6 sm:p-8 space-y-4"
          >
            <div className="grid sm:grid-cols-2 gap-4">
              <Field label="Name" id="name">
                <input
                  id="name"
                  required
                  maxLength={100}
                  value={form.name}
                  onChange={(e) => setForm({ ...form, name: e.target.value })}
                  className="w-full bg-secondary/50 border border-border rounded-lg px-4 py-3 text-sm focus:outline-none focus:border-primary transition-colors"
                  placeholder="Your name"
                />
              </Field>
              <Field label="Email" id="email">
                <input
                  id="email"
                  type="email"
                  required
                  maxLength={255}
                  value={form.email}
                  onChange={(e) => setForm({ ...form, email: e.target.value })}
                  className="w-full bg-secondary/50 border border-border rounded-lg px-4 py-3 text-sm focus:outline-none focus:border-primary transition-colors"
                  placeholder="you@example.com"
                />
              </Field>
            </div>
            <Field label="Subject" id="subject">
              <input
                id="subject"
                maxLength={150}
                value={form.subject}
                onChange={(e) => setForm({ ...form, subject: e.target.value })}
                className="w-full bg-secondary/50 border border-border rounded-lg px-4 py-3 text-sm focus:outline-none focus:border-primary transition-colors"
                placeholder="Internship opportunity"
              />
            </Field>
            <Field label="Message" id="message">
              <textarea
                id="message"
                required
                maxLength={1500}
                rows={5}
                value={form.message}
                onChange={(e) => setForm({ ...form, message: e.target.value })}
                className="w-full bg-secondary/50 border border-border rounded-lg px-4 py-3 text-sm focus:outline-none focus:border-primary transition-colors resize-none"
                placeholder="Tell me about your project or opportunity..."
              />
            </Field>
            <button
              type="submit"
              className="w-full inline-flex items-center justify-center gap-2 px-6 py-3 rounded-lg bg-gradient-primary text-primary-foreground font-semibold shadow-glow hover:scale-[1.02] transition-transform"
            >
              {sent ? <><CheckCircle2 size={18} /> Message ready</> : <><Send size={18} /> Send Message</>}
            </button>
          </motion.form>
        </div>
      </div>
    </section>
  );
}

function Field({ label, id, children }: { label: string; id: string; children: React.ReactNode }) {
  return (
    <label htmlFor={id} className="block">
      <span className="block text-xs font-medium text-muted-foreground mb-1.5 uppercase tracking-widest">{label}</span>
      {children}
    </label>
  );
}

function Footer() {
  return (
    <footer className="relative border-t border-border py-10 px-6 mt-10">
      <div className="mx-auto max-w-7xl flex flex-col sm:flex-row items-center justify-between gap-4 text-sm text-muted-foreground">
        <div>
          © {new Date().getFullYear()} <span className="text-gradient font-semibold">Sravani Kallemolam</span>. Crafted with passion.
        </div>
        <div className="flex items-center gap-4">
          <a href="#top" className="hover:text-foreground transition-colors">Back to top ↑</a>
        </div>
      </div>
    </footer>
  );
}
