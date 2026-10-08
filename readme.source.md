```aura width=820 height=1080
<div style={{
  width: '100%',
  height: '100%',
  background: 'linear-gradient(150deg, #07080c 0%, #0d1117 50%, #080a10 100%)',
  display: 'flex',
  flexDirection: 'column',
  justifyContent: 'space-between',
  padding: '34px 38px',
  fontFamily: 'Inter, -apple-system, sans-serif',
  position: 'relative',
  overflow: 'hidden',
  borderRadius: 20,
  border: '1px solid rgba(255, 255, 255, 0.08)'
}}>
  <style>{`
    @keyframes pulse-slow {
      0%, 100% { transform: scale(1) translate(0, 0); opacity: 0.4; }
      50% { transform: scale(1.15) translate(30px, -20px); opacity: 0.8; }
    }
    @keyframes pulse-alt {
      0%, 100% { transform: scale(1.1) translate(0, 0); opacity: 0.3; }
      50% { transform: scale(0.95) translate(-25px, 20px); opacity: 0.65; }
    }
    #orb-cyan { animation: pulse-slow 9s ease-in-out infinite; }
    #orb-purple { animation: pulse-alt 11s ease-in-out infinite; }
  `}</style>

  {/* Ambient Background Aura Orbs */}
  <svg width="820" height="1080" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="grad-cyan" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(56, 189, 248, 0.5)" />
        <stop offset="60%" stopColor="rgba(56, 189, 248, 0.08)" />
        <stop offset="100%" stopColor="rgba(56, 189, 248, 0)" />
      </radialGradient>
      <radialGradient id="grad-purple" cx="50%" cy="50%" r="50%">
        <stop offset="0%" stopColor="rgba(168, 85, 247, 0.45)" />
        <stop offset="60%" stopColor="rgba(168, 85, 247, 0.08)" />
        <stop offset="100%" stopColor="rgba(168, 85, 247, 0)" />
      </radialGradient>
    </defs>
    <ellipse id="orb-cyan" cx="100" cy="100" rx="280" ry="200" fill="url(#grad-cyan)" />
    <ellipse id="orb-purple" cx="740" cy="380" rx="300" ry="240" fill="url(#grad-purple)" />
    <ellipse id="orb-cyan-2" cx="160" cy="880" rx="260" ry="180" fill="url(#grad-cyan)" opacity="0.4" />
  </svg>

  {/* =========================================
      1. HERO PROFILE HEADER
     ========================================= */}
  <div style={{ display: 'flex', flexDirection: 'column' }}>
    <div style={{
      display: 'flex',
      alignItems: 'center',
      gap: '8px',
      marginBottom: '8px'
    }}>
      <div style={{
        width: '8px',
        height: '8px',
        borderRadius: '50%',
        backgroundColor: '#22c55e',
        boxShadow: '0 0 10px #22c55e'
      }} />
      <div style={{
        fontSize: '12px',
        letterSpacing: '0.08em',
        textTransform: 'uppercase',
        color: '#94a3b8',
        fontWeight: 600
      }}>
        Available for projects & collaboration
      </div>
    </div>

    <div style={{ display: 'flex', alignItems: 'baseline', gap: '12px' }}>
      <div style={{
        fontSize: '32px',
        fontWeight: 700,
        color: '#f8fafc',
        letterSpacing: '-0.02em'
      }}>
        Dev Takkekar
      </div>
      <div style={{ fontSize: '16px', color: '#64748b', fontWeight: 400 }}>
        / devtakkekar
      </div>
    </div>

    <div style={{
      display: 'flex',
      fontSize: '14px',
      color: '#cbd5e1',
      marginTop: '6px',
      lineHeight: '1.4'
    }}>
      Building lightweight developer utilities, game scripts & interactive web apps.
    </div>

    <div style={{
      display: 'flex',
      gap: '18px',
      marginTop: '10px',
      fontSize: '12px',
      color: '#94a3b8'
    }}>
      <div>📍 Mumbai</div>
      <div>⚡ Go • JavaScript • Python • Lua • React</div>
      <div>🎮 Gamer & Developer</div>
    </div>
  </div>

  {/* =========================================
      2. MOST USED LANGUAGES BREAKDOWN
     ========================================= */}
  <div style={{
    background: 'rgba(255, 255, 255, 0.03)',
    borderRadius: '14px',
    border: '1px solid rgba(255, 255, 255, 0.06)',
    padding: '14px 18px',
    display: 'flex',
    flexDirection: 'column'
  }}>
    <div style={{
      display: 'flex',
      justifyContent: 'space-between',
      alignItems: 'center',
      marginBottom: '10px'
    }}>
      <div style={{ fontSize: '13px', fontWeight: 600, color: '#f1f5f9' }}>
        📊 Most Used Languages
      </div>
      <div style={{ fontSize: '11px', color: '#64748b' }}>
        Based on GitHub repositories
      </div>
    </div>

    <div style={{
      display: 'flex',
      width: '100%',
      height: '8px',
      borderRadius: '6px',
      overflow: 'hidden',
      backgroundColor: '#1e293b',
      marginBottom: '10px'
    }}>
      <div style={{ width: '40%', height: '100%', backgroundColor: '#00ADD8' }} />
      <div style={{ width: '30%', height: '100%', backgroundColor: '#F7DF1E' }} />
      <div style={{ width: '15%', height: '100%', backgroundColor: '#6366f1' }} />
      <div style={{ width: '10%', height: '100%', backgroundColor: '#3572A5' }} />
      <div style={{ width: '5%', height: '100%', backgroundColor: '#E34C26' }} />
    </div>

    <div style={{ display: 'flex', alignItems: 'center', gap: '20px' }}>
      {[
        { name: 'Go', pct: '40.0%', color: '#00ADD8' },
        { name: 'JavaScript', pct: '30.0%', color: '#F7DF1E' },
        { name: 'Lua', pct: '15.0%', color: '#6366f1' },
        { name: 'Python', pct: '10.0%', color: '#3572A5' },
        { name: 'HTML/CSS', pct: '5.0%', color: '#E34C26' }
      ].map(lang => (
        <div key={lang.name} style={{ display: 'flex', alignItems: 'center', gap: '6px' }}>
          <div style={{ width: '7px', height: '7px', borderRadius: '50%', backgroundColor: lang.color }} />
          <div style={{ fontSize: '12px', fontWeight: 500, color: '#cbd5e1' }}>{lang.name}</div>
          <div style={{ fontSize: '11px', color: '#64748b' }}>{lang.pct}</div>
        </div>
      ))}
    </div>
  </div>

  {/* =========================================
      3. TECHNOLOGIES & TOOLS
     ========================================= */}
  <div style={{
    background: 'rgba(255, 255, 255, 0.03)',
    borderRadius: '14px',
    border: '1px solid rgba(255, 255, 255, 0.06)',
    padding: '14px 18px',
    display: 'flex',
    flexDirection: 'column'
  }}>
    <div style={{
      display: 'flex',
      justifyContent: 'space-between',
      alignItems: 'center',
      marginBottom: '10px'
    }}>
      <div style={{ fontSize: '13px', fontWeight: 600, color: '#f1f5f9' }}>
        💻 Technologies & Tools
      </div>
      <div style={{ fontSize: '11px', color: '#64748b' }}>
        Frameworks, Languages & Cloud
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: '8px' }}>
      {/* Languages & Core */}
      <div style={{ display: 'flex', alignItems: 'center', gap: '8px' }}>
        <div style={{ fontSize: '11px', color: '#64748b', width: '85px' }}>Languages:</div>
        <div style={{ display: 'flex', gap: '6px' }}>
          {['Go', 'Python', 'JavaScript', 'TypeScript', 'Lua', 'Java', '.NET', 'HTML5', 'CSS3', 'Tailwind'].map(item => (
            <div key={item} style={{
              fontSize: '11px',
              color: '#e2e8f0',
              background: 'rgba(255, 255, 255, 0.05)',
              border: '1px solid rgba(255, 255, 255, 0.08)',
              padding: '2px 7px',
              borderRadius: '5px'
            }}>
              {item}
            </div>
          ))}
        </div>
      </div>

      {/* Frameworks & Databases */}
      <div style={{ display: 'flex', alignItems: 'center', gap: '8px' }}>
        <div style={{ fontSize: '11px', color: '#64748b', width: '85px' }}>Frameworks:</div>
        <div style={{ display: 'flex', gap: '6px' }}>
          {['React.js', 'Next.js', 'Node.js', 'Express', 'MongoDB', 'PostgreSQL', 'MySQL', 'Firebase', 'Realm'].map(item => (
            <div key={item} style={{
              fontSize: '11px',
              color: '#e2e8f0',
              background: 'rgba(255, 255, 255, 0.05)',
              border: '1px solid rgba(255, 255, 255, 0.08)',
              padding: '2px 7px',
              borderRadius: '5px'
            }}>
              {item}
            </div>
          ))}
        </div>
      </div>

      {/* Tools & AI/ML */}
      <div style={{ display: 'flex', alignItems: 'center', gap: '8px' }}>
        <div style={{ fontSize: '11px', color: '#64748b', width: '85px' }}>Tools & ML:</div>
        <div style={{ display: 'flex', gap: '6px' }}>
          {['Git', 'Linux', 'AWS', 'Android Studio', 'Figma', 'Jupyter', 'Pandas', 'NumPy', 'Scikit-learn'].map(item => (
            <div key={item} style={{
              fontSize: '11px',
              color: '#e2e8f0',
              background: 'rgba(255, 255, 255, 0.05)',
              border: '1px solid rgba(255, 255, 255, 0.08)',
              padding: '2px 7px',
              borderRadius: '5px'
            }}>
              {item}
            </div>
          ))}
        </div>
      </div>
    </div>
  </div>

  {/* =========================================
      4. RECENT PROJECTS (2x2 GRID)
     ========================================= */}
  <div style={{ display: 'flex', flexDirection: 'column' }}>
    <div style={{
      display: 'flex',
      justifyContent: 'space-between',
      alignItems: 'center',
      marginBottom: '10px'
    }}>
      <div style={{ fontSize: '13px', fontWeight: 600, color: '#f1f5f9' }}>
        🚀 Recent Projects
      </div>
      <div style={{ fontSize: '11px', color: '#64748b' }}>
        Featured Highlights
      </div>
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: '10px' }}>
      {/* Row 1 */}
      <div style={{ display: 'flex', gap: '12px' }}>
        {[
          {
            title: 'dev-sync',
            desc: 'Real-time lightweight cross-platform directory synchronizer for rapid developer workflows.',
            lang: 'Go',
            color: '#00ADD8',
            tag: 'CLI Utility'
          },
          {
            title: 'qb-foodorder',
            desc: 'Dynamic QBCore framework food ordering system with an interactive custom UI.',
            lang: 'JavaScript / Lua',
            color: '#F7DF1E',
            tag: 'FiveM Script'
          }
        ].map(repo => (
          <div key={repo.title} style={{
            flex: 1,
            background: 'rgba(255, 255, 255, 0.03)',
            borderRadius: '12px',
            border: '1px solid rgba(255, 255, 255, 0.06)',
            padding: '13px 15px',
            display: 'flex',
            flexDirection: 'column',
            justifyContent: 'space-between'
          }}>
            <div style={{ display: 'flex', flexDirection: 'column' }}>
              <div style={{
                display: 'flex',
                alignItems: 'center',
                justifyContent: 'space-between',
                marginBottom: '6px'
              }}>
                <div style={{ fontSize: '14px', fontWeight: 600, color: '#38bdf8' }}>
                  {repo.title}
                </div>
                <div style={{
                  fontSize: '10px',
                  color: '#94a3b8',
                  background: 'rgba(255, 255, 255, 0.06)',
                  padding: '2px 6px',
                  borderRadius: '5px'
                }}>
                  {repo.tag}
                </div>
              </div>
              <div style={{ fontSize: '11px', color: '#94a3b8', lineHeight: '1.4' }}>
                {repo.desc}
              </div>
            </div>

            <div style={{
              display: 'flex',
              alignItems: 'center',
              gap: '6px',
              marginTop: '10px'
            }}>
              <div style={{ width: '7px', height: '7px', borderRadius: '50%', backgroundColor: repo.color }} />
              <div style={{ fontSize: '11px', color: '#cbd5e1' }}>{repo.lang}</div>
            </div>
          </div>
        ))}
      </div>

      {/* Row 2 */}
      <div style={{ display: 'flex', gap: '12px' }}>
        {[
          {
            title: 'notes.io',
            desc: 'Minimalistic, distraction-free notes web application with seamless local state.',
            lang: 'React.js',
            color: '#61DAFB',
            tag: 'Web App'
          },
          {
            title: 'coc-bot',
            desc: 'Automated Clash of Clans player, war & clan stats tracking Discord bot utility.',
            lang: 'Node.js',
            color: '#68A063',
            tag: 'Discord Bot'
          }
        ].map(repo => (
          <div key={repo.title} style={{
            flex: 1,
            background: 'rgba(255, 255, 255, 0.03)',
            borderRadius: '12px',
            border: '1px solid rgba(255, 255, 255, 0.06)',
            padding: '13px 15px',
            display: 'flex',
            flexDirection: 'column',
            justifyContent: 'space-between'
          }}>
            <div style={{ display: 'flex', flexDirection: 'column' }}>
              <div style={{
                display: 'flex',
                alignItems: 'center',
                justifyContent: 'space-between',
                marginBottom: '6px'
              }}>
                <div style={{ fontSize: '14px', fontWeight: 600, color: '#38bdf8' }}>
                  {repo.title}
                </div>
                <div style={{
                  fontSize: '10px',
                  color: '#94a3b8',
                  background: 'rgba(255, 255, 255, 0.06)',
                  padding: '2px 6px',
                  borderRadius: '5px'
                }}>
                  {repo.tag}
                </div>
              </div>
              <div style={{ fontSize: '11px', color: '#94a3b8', lineHeight: '1.4' }}>
                {repo.desc}
              </div>
            </div>

            <div style={{
              display: 'flex',
              alignItems: 'center',
              gap: '6px',
              marginTop: '10px'
            }}>
              <div style={{ width: '7px', height: '7px', borderRadius: '50%', backgroundColor: repo.color }} />
              <div style={{ fontSize: '11px', color: '#cbd5e1' }}>{repo.lang}</div>
            </div>
          </div>
        ))}
      </div>
    </div>
  </div>

  {/* =========================================
      5. CONNECT / FOOTER SECTION
     ========================================= */}
  <div style={{
    display: 'flex',
    alignItems: 'center',
    justifyContent: 'space-between',
    paddingTop: '16px',
    borderTop: '1px solid rgba(255, 255, 255, 0.08)'
  }}>
    <div style={{ display: 'flex', flexDirection: 'column', gap: '2px' }}>
      <div style={{ fontSize: '13px', fontWeight: 600, color: '#f1f5f9' }}>
        📬 Let's Connect
      </div>
      <div style={{ fontSize: '11px', color: '#64748b' }}>
        Open for collaborations & developer inquiries
      </div>
    </div>
    <div style={{
      display: 'flex',
      alignItems: 'center',
      gap: '8px',
      background: 'rgba(56, 189, 248, 0.08)',
      border: '1px solid rgba(56, 189, 248, 0.25)',
      borderRadius: '8px',
      padding: '7px 16px'
    }}>
      <div style={{ fontSize: '12px', color: '#38bdf8', fontWeight: 500 }}>
        ✉ devtakkekar@gmail.com
      </div>
    </div>
  </div>
</div>
```
