
  return (
    <div className="relative min-h-screen overflow-hidden bg-black text-cyan-300 font-mono">
      {/* Animated Background */}
      <div className="absolute inset-0 bg-[radial-gradient(circle_at_center,_rgba(0,255,255,0.15),_transparent_40%)] animate-pulse"></div>

      <div className="absolute inset-0 overflow-hidden">
        {[...Array(60)].map((_, i) => (
          <div
            key={i}
            className="absolute bg-cyan-400 rounded-full opacity-40 animate-ping"
            style={{
              width: `${Math.random() * 4 + 1}px`,
              height: `${Math.random() * 4 + 1}px`,
              left: `${Math.random() * 100}%`,
              top: `${Math.random() * 100}%`,
              animationDuration: `${Math.random() * 6 + 2}s`,
            }}
          />
        ))}
      </div>

      {/* Roaming Boy */}
      <div className="fixed bottom-8 left-0 z-50 animate-[walk_18s_linear_infinite]">
        <div className="relative">
          <div className="w-16 h-20 bg-cyan-400 rounded-t-full shadow-[0_0_40px_cyan] flex items-center justify-center text-black font-bold text-xl">
            😎
          </div>
          <div className="absolute -bottom-4 left-2 w-4 h-10 bg-cyan-300 animate-bounce"></div>
          <div className="absolute -bottom-4 right-2 w-4 h-10 bg-cyan-300 animate-bounce"></div>
        </div>
      </div>

      {/* Main Content */}
      <div className="relative z-10 flex flex-col items-center justify-center min-h-screen px-6 text-center">
        <div className="backdrop-blur-xl border border-cyan-500/30 bg-white/5 p-10 rounded-3xl shadow-[0_0_60px_rgba(0,255,255,0.25)] max-w-5xl">
          <h1 className="text-6xl md:text-8xl font-black tracking-widest text-transparent bg-clip-text bg-gradient-to-r from-cyan-400 via-blue-500 to-purple-500 animate-pulse">
            SASI.OS
          </h1>

          <p className="mt-6 text-lg md:text-2xl text-cyan-200 leading-relaxed">
            A futuristic developer universe powered by AI, code, caffeine,
            chaos, and sleepless nights.
          </p>

          <div className="mt-10 grid grid-cols-1 md:grid-cols-3 gap-6">
            {[
              {
                title: "MISSION",
                text: "Building insane full-stack & AI systems.",
              },
              {
                title: "STATUS",
                text: "Grinding DSA and escaping tutorial hell.",
              },
              {
                title: "SYSTEM",
                text: "Neural core stable. Sleep module corrupted.",
              },
            ].map((card, i) => (
              <div
                key={i}
                className="group border border-cyan-400/20 bg-black/40 p-6 rounded-2xl hover:scale-105 transition-all duration-500 hover:shadow-[0_0_30px_cyan]"
              >
                <h2 className="text-2xl font-bold text-cyan-300 mb-4 group-hover:text-white transition-all">
                  {card.title}
                </h2>
                <p className="text-cyan-100 text-sm leading-relaxed">
                  {card.text}
                </p>
              </div>
            ))}
          </div>

          {/* Terminal */}
          <div className="mt-12 text-left bg-black/80 border border-cyan-400/20 rounded-2xl p-6 shadow-[0_0_30px_rgba(0,255,255,0.15)]">
            <p className="text-green-400">&gt; boot_sequence</p>
            <p>Initializing neural systems...</p>
            <p>Loading GitHub archives...</p>
            <p>Injecting caffeine...</p>
            <p className="text-red-400">Sleep schedule not found.</p>
            <p className="text-cyan-300 mt-4">&gt; access developer_profile</p>
            <p>ACCESS GRANTED.</p>
          </div>

          {/* XP Bars */}
          <div className="mt-12 space-y-6 text-left">
            {[
              ["Python", "85%"],
              ["React", "75%"],
              ["AI/ML", "65%"],
              ["Backend", "80%"],
            ].map(([skill, level], i) => (
              <div key={i}>
                <div className="flex justify-between mb-2 text-cyan-200">
                  <span>{skill}</span>
                  <span>{level}</span>
                </div>
                <div className="w-full h-4 bg-black rounded-full overflow-hidden border border-cyan-400/20">
                  <div
                    className="h-full bg-gradient-to-r from-cyan-400 to-blue-500 shadow-[0_0_20px_cyan] animate-pulse"
                    style={{ width: level }}
                  />
                </div>
              </div>
            ))}
          </div>

          {/* Floating Buttons */}
          <div className="mt-12 flex flex-wrap gap-4 justify-center">
            {[
              "ENTER SYSTEM",
              "OPEN ARCHIVES",
              "VIEW PROJECTS",
              "START MISSION",
            ].map((btn, i) => (
              <button
                key={i}
                className="px-6 py-3 rounded-full border border-cyan-400/30 bg-cyan-400/10 hover:bg-cyan-400 hover:text-black transition-all duration-500 shadow-[0_0_20px_rgba(0,255,255,0.25)] hover:shadow-[0_0_40px_cyan]"
              >
                {btn}
              </button>
            ))}
          </div>
        </div>
      </div>

      {/* Floating Glitch Text */}
      <div className="absolute top-10 left-10 text-cyan-400 opacity-30 animate-pulse text-sm tracking-widest">
        SYSTEM ACTIVE
      </div>

      <div className="absolute bottom-10 right-10 text-red-400 opacity-40 animate-bounce text-sm tracking-widest">
        UNKNOWN SIGNAL DETECTED
      </div>

      {/* Custom Animation */}
      <style>{`
        @keyframes walk {
          0% {
            transform: translateX(-100px);
          }
          100% {
            transform: translateX(calc(100vw + 100px));
          }
        }
      `}</style>
    </div>
  );
}
