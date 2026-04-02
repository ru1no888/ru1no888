export default function ThanakornIntroPage() {
  const tech = [
    'ESP32',
    'Arduino',
    'MQTT',
    'C',
 ([github.com](https://github.com/ru1no888))ava',
    'Python',
    'FastAPI',
    'Node.js',
    'Next.js',
    'React',
    'Tailwind CSS',
    'SQL',
    'Git',
    'GitHub',
    'Linux',
  ];

  const projects = [
    {
      title: 'Smart Health Monitoring System',
      subtitle: 'Thesis Project',
      description:
        'Wearable IoT solution for real-time health data acquisition, transmission, and analysis.',
    },
    {
      title: 'IoT Security Matrix',
      subtitle: 'Embedded Security',
      description:
        'ESP32-based security infrastructure with multi-sensor synchronization and robust event handling.',
    },
    {
      title: 'Full-stack Web Applications',
      subtitle: 'Web Engineering',
      description:
        'Modern, high-performance platforms with clean architecture and efficient API design.',
    },
    {
      title: 'Automation Systems',
      subtitle: 'AI + Workflow',
      description:
        'AI-based scripts and bots to optimize workflows and reduce repetitive operations.',
    },
  ];

  return (
    <div className="min-h-screen bg-neutral-950 text-white overflow-hidden">
      <div className="absolute inset-0 bg-[radial-gradient(circle_at_top_right,rgba(59,130,246,0.22),transparent_30%),radial-gradient(circle_at_left,rgba(168,85,247,0.18),transparent_25%),linear-gradient(to_bottom,rgba(255,255,255,0.02),rgba(255,255,255,0))]" />

      <main className="relative mx-auto max-w-6xl px-6 py-10 md:px-10 md:py-16">
        <section className="grid items-center gap-10 lg:grid-cols-[1.3fr_0.9fr]">
          <div>
            <p className="mb-4 inline-flex rounded-full border border-white/10 bg-white/5 px-4 py-1 text-sm tracking-wide text-white/70 backdrop-blur">
              Portfolio / Introduction
            </p>
            <h1 className="max-w-4xl text-4xl font-black leading-tight md:text-6xl">
              Thanakorn <span className="text-cyan-400">Supawanchai</span>
            </h1>
            <p className="mt-3 text-lg text-white/70 md:text-2xl">
              Film — Computer Engineering Student
            </p>
            <p className="mt-6 max-w-2xl text-base leading-8 text-white/75 md:text-lg">
              I build practical technology from device to cloud — combining
              IoT architecture, embedded systems, backend engineering, and
              modern web development into reliable real-world solutions.
            </p>

            <div className="mt-8 flex flex-wrap gap-3">
              {['IoT & Embedded', 'Full-stack Developer', 'System Design', 'AI Automation'].map((item) => (
                <span
                  key={item}
                  className="rounded-full border border-cyan-400/20 bg-cyan-400/10 px-4 py-2 text-sm text-cyan-300"
                >
                  {item}
                </span>
              ))}
            </div>

            <div className="mt-8 flex flex-wrap gap-4">
              <a
                href="https://github.com/ru1no888"
                className="rounded-2xl bg-white px-6 py-3 text-sm font-semibold text-black transition hover:scale-[1.02]"
              >
                View GitHub
              </a>
              <a
                href="mailto:film.thanakorn39@gmail.com"
                className="rounded-2xl border border-white/15 bg-white/5 px-6 py-3 text-sm font-semibold text-white transition hover:bg-white/10"
              >
                Contact Me
              </a>
            </div>
          </div>

          <div className="relative">
            <div className="rounded-[32px] border border-white/10 bg-white/5 p-6 shadow-2xl backdrop-blur-xl">
              <div className="rounded-[28px] border border-white/10 bg-black/40 p-6">
                <p className="text-sm uppercase tracking-[0.25em] text-cyan-300/80">About Me</p>
                <div className="mt-4 space-y-4 text-white/75 leading-7">
                  <p>Focused on real-world engineering impact.</p>
                  <p>Passionate about IoT, embedded systems, and full-stack development.</p>
                  <p>Currently improving system design, backend performance, and AI automation.</p>
                  <p className="text-white">Goal: Build practical technology that solves real problems.</p>
                </div>
              </div>
            </div>
          </div>
        </section>

        <section className="mt-16 grid gap-6 md:grid-cols-2 xl:grid-cols-4">
          {projects.map((project) => (
            <div
              key={project.title}
              className="rounded-3xl border border-white/10 bg-white/[0.04] p-6 shadow-lg backdrop-blur-sm transition hover:-translate-y-1 hover:bg-white/[0.06]"
            >
              <p className="text-xs uppercase tracking-[0.25em] text-cyan-300/70">{project.subtitle}</p>
              <h3 className="mt-3 text-xl font-bold">{project.title}</h3>
              <p className="mt-3 leading-7 text-white/70">{project.description}</p>
            </div>
          ))}
        </section>

        <section className="mt-16 grid gap-8 lg:grid-cols-[1fr_1.1fr]">
          <div className="rounded-[28px] border border-white/10 bg-white/[0.04] p-7 backdrop-blur-sm">
            <p className="text-sm uppercase tracking-[0.25em] text-purple-300/80">Current Focus</p>
            <ul className="mt-5 space-y-4 text-white/75 leading-7">
              <li>Smarter IoT workflows with reliable real-time telemetry</li>
              <li>Backend performance and API response consistency</li>
              <li>Production-ready full-stack deployment skills</li>
              <li>Secure architecture from embedded devices to cloud services</li>
            </ul>
          </div>

          <div className="rounded-[28px] border border-white/10 bg-white/[0.04] p-7 backdrop-blur-sm">
            <p className="text-sm uppercase tracking-[0.25em] text-pink-300/80">Tech Stack</p>
            <div className="mt-5 flex flex-wrap gap-3">
              {tech.map((item) => (
                <span
                  key={item}
                  className="rounded-2xl border border-white/10 bg-black/30 px-4 py-2 text-sm text-white/80"
                >
                  {item}
                </span>
              ))}
            </div>
          </div>
        </section>

        <section className="mt-16 rounded-[32px] border border-white/10 bg-gradient-to-r from-cyan-500/10 via-transparent to-purple-500/10 p-8 backdrop-blur-sm">
          <p className="text-sm uppercase tracking-[0.3em] text-white/50">Signature</p>
          <h2 className="mt-3 text-2xl font-bold md:text-3xl">Code, Build, Improve, Repeat.</h2>
          <p className="mt-4 max-w-2xl text-white/70 leading-7">
            A sleek one-page introduction inspired by your GitHub profile, designed to present you as a builder focused on practical engineering, modern systems, and impactful software.
          </p>
        </section>
      </main>
    </div>
  );
}
