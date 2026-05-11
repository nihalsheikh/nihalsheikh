```aura width=860 height=260
<div style={{
  width:'100%', height:'100%', background:'#08080c',
  display:'flex', alignItems:'center', fontFamily:'Inter',
  position:'relative', overflow:'hidden', borderRadius:16,
  border:'1px solid rgba(110,80,220,0.2)',
}}>

  <style>{`
    @keyframes float-slow   { 0%,100%{transform:translateX(0px);opacity:0.8} 50%{transform:translateX(340px);opacity:1.1} }
    @keyframes float-medium { 0%,100%{transform:translateX(0px);opacity:0.7} 50%{transform:translateX(-240px);opacity:1.0} }
    @keyframes float-fast   { 0%,100%{transform:translateX(0px);opacity:0.9} 50%{transform:translateX(190px);opacity:0.6} }
    @keyframes float-lime   { 0%,100%{transform:translateX(0px);opacity:0.5} 50%{transform:translateX(-180px);opacity:0.9} }
    @keyframes float-wave   { 0%,100%{transform:translateX(0px);opacity:0.6} 33%{transform:translateX(-150px);opacity:0.85} 66%{transform:translateX(80px);opacity:1.0} }
    @keyframes float-pulse  { 0%,100%{transform:scale(1);opacity:0.7} 50%{transform:scale(1.25);opacity:0.35} }
    #hh-1 { animation: float-slow   8s  ease-in-out infinite; }
    #hh-2 { animation: float-medium 12s ease-in-out infinite; }
    #hh-3 { animation: float-fast   9s  ease-in-out infinite; }
    #hh-4 { animation: float-lime   11s ease-in-out infinite reverse; }
    #hh-5 { animation: float-wave   13s ease-in-out infinite; }
    #hh-6 { animation: float-pulse  7s  ease-in-out infinite; }
    #hh-7 { animation: float-slow   14s ease-in-out infinite reverse; }
  `}</style>

  <svg width="860" height="260" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="hg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(110,20,210,0.75)" />
        <stop offset="40%" stopColor="rgba(90,15,180,0.32)" />
        <stop offset="70%" stopColor="rgba(90,15,180,0)" />
      </radialGradient>
      <radialGradient id="hg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(40,60,255,0.58)" />
        <stop offset="45%" stopColor="rgba(30,50,200,0.22)" />
        <stop offset="70%" stopColor="rgba(30,50,200,0)" />
      </radialGradient>
      <radialGradient id="hg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(0,130,255,0.42)" />
        <stop offset="50%" stopColor="rgba(0,100,220,0.16)" />
        <stop offset="70%" stopColor="rgba(0,100,220,0)" />
      </radialGradient>
      <radialGradient id="hg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(160,30,255,0.52)" />
        <stop offset="45%" stopColor="rgba(130,20,220,0.20)" />
        <stop offset="70%" stopColor="rgba(130,20,220,0)" />
      </radialGradient>
      <radialGradient id="hg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(0,190,230,0.32)" />
        <stop offset="70%" stopColor="rgba(0,190,230,0)" />
      </radialGradient>
      <radialGradient id="hg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(90,30,200,0.38)" />
        <stop offset="70%" stopColor="rgba(90,30,200,0)" />
      </radialGradient>
      <radialGradient id="hg7" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(20,60,255,0.42)" />
        <stop offset="50%" stopColor="rgba(10,40,200,0.16)" />
        <stop offset="70%" stopColor="rgba(10,40,200,0)" />
      </radialGradient>
    </defs>
    <ellipse id="hh-1" cx="160" cy="280" rx="270" ry="220" fill="url(#hg1)" />
    <ellipse id="hh-2" cx="310" cy="280" rx="220" ry="180" fill="url(#hg2)" />
    <ellipse id="hh-3" cx="440" cy="275" rx="185" ry="160" fill="url(#hg3)" />
    <ellipse id="hh-4" cx="580" cy="285" rx="160" ry="145" fill="url(#hg4)" />
    <ellipse id="hh-5" cx="740" cy="285" rx="140" ry="130" fill="url(#hg5)" />
    <ellipse id="hh-6" cx="290" cy="275" rx="185" ry="160" fill="url(#hg6)" />
    <ellipse id="hh-7" cx="510" cy="270" rx="210" ry="185" fill="url(#hg7)" />
  </svg>

  <div style={{
    position:'absolute', left:44, top:0, bottom:0,
    display:'flex', alignItems:'center', justifyContent:'center',
  }}>
    <div style={{
      width:104, height:104, borderRadius:52,
      background:'linear-gradient(135deg, #6622ee 0%, #0088ff 100%)',
      display:'flex', alignItems:'center', justifyContent:'center',
    }}>
      <img src={github.user.avatarUrl} width={96} height={96} style={{ borderRadius:48 }} />
    </div>
  </div>

  <div style={{ display:'flex', flexDirection:'column', marginLeft:172, gap:9, paddingRight:36 }}>

    <div style={{ display:'flex', fontSize:36, fontWeight:800, color:'#ffffff', letterSpacing:'-0.5px', lineHeight:1 }}>
      {github.user.name || github.user.login}
    </div>

    <div style={{ display:'flex', fontSize:14, color:'rgba(180,165,255,0.82)', fontWeight:500, letterSpacing:'0.2px' }}>
      Software Engineer · Fullstack Developer · Web3 Enthusiast
    </div>

    <div style={{ display:'flex', gap:18, fontSize:12, color:'rgba(150,140,200,0.72)', fontWeight:500 }}>
      <div style={{ display:'flex' }}>📍 India</div>
    </div>

    <div style={{ display:'flex', fontSize:12, color:'rgba(140,180,255,0.75)', fontWeight:500 }}>
      🔨 Currently building SnippetVault &nbsp;·&nbsp; 🚀 Open to full-time &amp; freelance
    </div>

    <div style={{ display:'flex', gap:7, marginTop:2 }}>
      {['Python', 'TypeScript', 'JavaScript', 'React', 'Next.js'].map(function(tag) {
        return (
          <div key={tag} style={{
            display:'flex', padding:'4px 13px', borderRadius:20,
            background:'rgba(80,40,220,0.20)', border:'1px solid rgba(110,80,240,0.38)',
            color:'rgba(205,195,255,0.88)', fontSize:12, fontWeight:700,
          }}>{tag}</div>
        );
      })}
    </div>

  </div>

</div>
```

```aura width=860 height=110
<div style={{
  width:'100%', height:'100%', background:'#08080c',
  display:'flex', alignItems:'center', justifyContent:'center',
  fontFamily:'Inter', position:'relative', overflow:'hidden',
  borderRadius:16, border:'1px solid rgba(80,60,200,0.18)',
}}>

  <style>{`
    @keyframes sg1-drift { 0%,100%{transform:translateX(0);opacity:0.55} 50%{transform:translateX(200px);opacity:0.85} }
    @keyframes sg2-drift { 0%,100%{transform:translateX(0);opacity:0.45} 50%{transform:translateX(-160px);opacity:0.80} }
    #sg1 { animation: sg1-drift 14s ease-in-out infinite; }
    #sg2 { animation: sg2-drift 11s ease-in-out infinite reverse; }
  `}</style>

  <svg width="860" height="110" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="sg1g" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(40,80,255,0.48)" />
        <stop offset="70%" stopColor="rgba(40,80,255,0)" />
      </radialGradient>
      <radialGradient id="sg2g" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(130,30,255,0.42)" />
        <stop offset="70%" stopColor="rgba(130,30,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="sg1" cx="200" cy="110" rx="280" ry="150" fill="url(#sg1g)" />
    <ellipse id="sg2" cx="660" cy="110" rx="240" ry="140" fill="url(#sg2g)" />
  </svg>

  {[
    { value: github.stats.totalRepos,   label: 'REPOS',   color: 'rgba(100,170,255,1)'  },
    { value: github.stats.totalStars,   label: 'STARS',   color: 'rgba(255,200,80,1)'   },
    { value: github.stats.totalCommits, label: 'COMMITS', color: 'rgba(180,130,255,1)'  },
  ].map(function(stat, i) {
    return (
      <div key={stat.label} style={{
        display:'flex', flexDirection:'column', alignItems:'center', justifyContent:'center',
        flex:1, gap:5,
        borderRight: i < 2 ? '1px solid rgba(80,60,180,0.20)' : 'none',
      }}>
        <div style={{ display:'flex', fontSize:44, fontWeight:800, color:stat.color, lineHeight:1, letterSpacing:'-1px' }}>
          {stat.value || '—'}
        </div>
        <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(120,110,170,0.55)', letterSpacing:'2.5px' }}>
          {stat.label}
        </div>
      </div>
    );
  })}

</div>
```

```aura width=860 height=280
<div style={{
  width:'100%', height:'100%', background:'#08080c',
  display:'flex', flexDirection:'column', justifyContent:'center',
  fontFamily:'Inter', position:'relative', overflow:'hidden',
  borderRadius:16, border:'1px solid rgba(110,80,220,0.18)',
  padding:'0 40px',
}}>

  <style>{`
    @keyframes ts-drift { 0%,100%{transform:translateX(0);opacity:0.5} 50%{transform:translateX(220px);opacity:0.8} }
    #ts-bg { animation: ts-drift 14s ease-in-out infinite; }
  `}</style>

  <svg width="860" height="280" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="tg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(110,20,210,0.42)" />
        <stop offset="70%" stopColor="rgba(110,20,210,0)" />
      </radialGradient>
    </defs>
    <ellipse id="ts-bg" cx="90" cy="240" rx="340" ry="210" fill="url(#tg1)" />
  </svg>

  <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(155,140,210,0.50)', letterSpacing:'3px', marginBottom:18 }}>
    TECH STACK
  </div>

  {[
    {
      label: 'LANGUAGES',
      tags:  ['Python', 'TypeScript', 'JavaScript', 'Java'],
      color: 'rgba(255,190,80,0.90)',
      bg:    'rgba(70,45,0,0.28)',
      border:'rgba(210,140,20,0.32)',
    },
    {
      label: 'FRONTEND',
      tags:  ['React', 'Next.js', 'Tailwind CSS', 'HTML5', 'CSS3'],
      color: 'rgba(110,195,255,0.92)',
      bg:    'rgba(10,45,100,0.28)',
      border:'rgba(40,120,255,0.32)',
    },
    {
      label: 'BACKEND & DB',
      tags:  ['PostgreSQL', 'MongoDB', 'MySQL', 'Prisma', 'Neon', 'Supabase', 'Zod'],
      color: 'rgba(175,145,255,0.92)',
      bg:    'rgba(55,25,130,0.26)',
      border:'rgba(110,65,245,0.32)',
    },
    {
      label: 'TOOLS & AI',
      tags:  ['Docker', 'Git', 'Linux', 'Vercel', 'Ollama', 'OpenRouter', 'Claude Code', 'Gemini CLI'],
      color: 'rgba(90,215,175,0.92)',
      bg:    'rgba(0,55,38,0.26)',
      border:'rgba(30,165,115,0.32)',
    },
  ].map(function(row) {
    return (
      <div key={row.label} style={{ display:'flex', alignItems:'center', gap:12, marginBottom:12 }}>
        <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(130,120,180,0.60)', letterSpacing:'1.5px', width:94, flexShrink:0 }}>
          {row.label}
        </div>
        <div style={{ display:'flex', gap:7, flexWrap:'wrap' }}>
          {row.tags.map(function(tag) {
            return (
              <div key={tag} style={{
                display:'flex', padding:'4px 12px', borderRadius:14,
                background:row.bg, border:'1px solid ' + row.border,
                color:row.color, fontSize:11, fontWeight:600,
              }}>{tag}</div>
            );
          })}
        </div>
      </div>
    );
  })}

</div>
```

```aura width=120 height=44 link="https://www.linkedin.com/in/nihalsheikh/" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/main/icons/linkedin-icon.png"
  text="LinkedIn"
  backgroundColor="#000000"
  width={120}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#b57af9' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#9d6bf0' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#c89dfb' },
  ]}
/>
```

```aura width=138 height=44 link="https://x.com/sshNihal" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/main/icons/x-icon.svg"
  text="Twitter / X"
  backgroundColor="#000000"
  width={138}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#818cf8' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#9298f8' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#7479f5' },
  ]}
/>
```

```aura width=138 height=44 link="https://flowcv.me/nihalsheikh" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/main/icons/globe.svg"
  text="Portfolio"
  backgroundColor="#000000"
  width={138}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#818cf8' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#9298f8' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#7479f5' },
  ]}
/>
```

```aura width=110 height=44 link="mailto:nihalsheikh585@gmail.com" inline align=center
<SocialMediaButton
  icon="https://raw.githubusercontent.com/nihalsheikh/nihalsheikh/main/icons/gmail-icon.svg"
  text="Email"
  backgroundColor="#000000"
  width={110}
  height={44}
  gradientStops={[
    { offset: '0%', color: '#d855f7' },
    { offset: '30%', color: '#000000' },
    { offset: '60%', color: '#b557e8' },
    { offset: '80%', color: '#000000' },
    { offset: '100%', color: '#cc6ef9' },
  ]}
/>
```

<br>
<p align="center"><sub>nihalsheikh &nbsp;·&nbsp; fueled by chai and compile errors ☕</sub></p>
