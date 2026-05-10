```aura width=800 height=200
<div style={{
  width: '100%', height: '100%', background: '#08080c',
  display: 'flex', alignItems: 'center', fontFamily: 'Inter',
  position: 'relative', overflow: 'hidden', borderRadius: 16,
  border: '1px solid rgba(110,80,220,0.2)'
}}>

  <style>{`
    @keyframes float-slow    { 0%,100%{transform:translateX(0px);opacity:0.8} 50%{transform:translateX(340px);opacity:1.1} }
    @keyframes float-medium  { 0%,100%{transform:translateX(0px);opacity:0.7} 50%{transform:translateX(-240px);opacity:1.0} }
    @keyframes float-fast    { 0%,100%{transform:translateX(0px);opacity:0.9} 50%{transform:translateX(190px);opacity:0.6} }
    @keyframes float-lime    { 0%,100%{transform:translateX(0px);opacity:0.5} 50%{transform:translateX(-180px);opacity:0.9} }
    @keyframes float-wave    { 0%,100%{transform:translateX(0px);opacity:0.6} 33%{transform:translateX(-150px);opacity:0.85} 66%{transform:translateX(80px);opacity:1.0} }
    @keyframes float-pulse   { 0%,100%{transform:scale(1);opacity:0.7} 50%{transform:scale(1.25);opacity:0.35} }
    #gh-1 { animation: float-slow   8s  ease-in-out infinite; }
    #gh-2 { animation: float-medium 12s ease-in-out infinite; }
    #gh-3 { animation: float-fast   9s  ease-in-out infinite; }
    #gh-4 { animation: float-lime   11s ease-in-out infinite reverse; }
    #gh-5 { animation: float-wave   13s ease-in-out infinite; }
    #gh-6 { animation: float-pulse  7s  ease-in-out infinite; }
    #gh-7 { animation: float-slow   14s ease-in-out infinite reverse; }
  `}</style>

  <svg width="860" height="200" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="rg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(110,20,210,0.75)" />
        <stop offset="40%" stopColor="rgba(90,15,180,0.32)" />
        <stop offset="70%" stopColor="rgba(90,15,180,0)" />
      </radialGradient>
      <radialGradient id="rg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(40,60,255,0.58)" />
        <stop offset="45%" stopColor="rgba(30,50,200,0.22)" />
        <stop offset="70%" stopColor="rgba(30,50,200,0)" />
      </radialGradient>
      <radialGradient id="rg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(0,130,255,0.42)" />
        <stop offset="50%" stopColor="rgba(0,100,220,0.16)" />
        <stop offset="70%" stopColor="rgba(0,100,220,0)" />
      </radialGradient>
      <radialGradient id="rg4" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(212,255,0,0.38)" />
        <stop offset="45%" stopColor="rgba(180,220,0,0.14)" />
        <stop offset="70%" stopColor="rgba(180,220,0,0)" />
      </radialGradient>
      <radialGradient id="rg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(160,30,255,0.52)" />
        <stop offset="45%" stopColor="rgba(130,20,220,0.20)" />
        <stop offset="70%" stopColor="rgba(130,20,220,0)" />
      </radialGradient>
      <radialGradient id="rg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(212,255,0,0.30)" />
        <stop offset="70%" stopColor="rgba(212,255,0,0)" />
      </radialGradient>
      <radialGradient id="rg7" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(20,60,255,0.38)" />
        <stop offset="70%" stopColor="rgba(20,60,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="gh-1" cx="160" cy="230" rx="270" ry="195" fill="url(#rg1)" />
    <ellipse id="gh-2" cx="310" cy="240" rx="220" ry="165" fill="url(#rg2)" />
    <ellipse id="gh-3" cx="430" cy="245" rx="185" ry="145" fill="url(#rg3)" />
    <ellipse id="gh-4" cx="560" cy="255" rx="160" ry="130" fill="url(#rg4)" />
    <ellipse id="gh-5" cx="730" cy="250" rx="140" ry="115" fill="url(#rg5)" />
    <ellipse id="gh-6" cx="290" cy="240" rx="185" ry="145" fill="url(#rg6)" />
    <ellipse id="gh-7" cx="500" cy="230" rx="210" ry="165" fill="url(#rg7)" />
  </svg>

  <div style={{
    position:'absolute', left:48, top:52, width:96, height:96,
    borderRadius:48,
    background:'linear-gradient(135deg, #6622ee 0%, #D4FF00 100%)',
    display:'flex', alignItems:'center', justifyContent:'center',
  }}>
    <img src={github.user.avatarUrl} width={88} height={88} style={{ borderRadius:44 }} />
  </div>

  <div style={{ display:'flex', flexDirection:'column', marginLeft:168, gap:10 }}>
    <div style={{ display:'flex', fontSize:36, fontWeight:800, color:'#ffffff', letterSpacing:'-1px', lineHeight:1 }}>
      {github.user.name || github.user.login}
    </div>
    <div style={{ display:'flex', fontSize:14, color:'rgba(190,180,255,0.85)', fontWeight:400, letterSpacing:'0.3px' }}>
      {github.user.bio || 'Full-Stack Engineer · Open Source Builder · AI Tinkerer'}
    </div>
    <div style={{ display:'flex', gap:8, marginTop:2 }}>
      {['Python', 'TypeScript', 'Next.js', 'React'].map(function(tag) {
        return (
          <div key={tag} style={{
            display:'flex', padding:'4px 13px', borderRadius:20,
            background:'rgba(80,40,220,0.20)', border:'1px solid rgba(110,80,240,0.35)',
            color:'rgba(212,255,0,0.90)', fontSize:12, fontWeight:700,
          }}>{tag}</div>
        );
      })}
    </div>
  </div>

</div>
```

```aura width=800 height=130
<div style={{
  width:'100%', height:'100%', background:'#08080c',
  display:'flex', alignItems:'center', justifyContent:'center',
  fontFamily:'Inter', position:'relative', overflow:'hidden',
  borderRadius:16, border:'1px solid rgba(110,80,220,0.18)',
}}>

  <style>{`
    @keyframes stat-glow-l { 0%,100%{transform:translateX(0);opacity:0.6} 50%{transform:translateX(120px);opacity:1.0} }
    @keyframes stat-glow-r { 0%,100%{transform:translateX(0);opacity:0.7} 50%{transform:translateX(-100px);opacity:0.9} }
    @keyframes stat-glow-c { 0%,100%{transform:scale(1);opacity:0.5} 50%{transform:scale(1.3);opacity:0.85} }
    #sg-l { animation: stat-glow-l 10s ease-in-out infinite; }
    #sg-r { animation: stat-glow-r 12s ease-in-out infinite; }
    #sg-c { animation: stat-glow-c 9s  ease-in-out infinite; }
  `}</style>

  <svg width="800" height="130" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="sg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(110,20,210,0.55)" />
        <stop offset="70%" stopColor="rgba(110,20,210,0)" />
      </radialGradient>
      <radialGradient id="sg2" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(212,255,0,0.35)" />
        <stop offset="70%" stopColor="rgba(212,255,0,0)" />
      </radialGradient>
      <radialGradient id="sg3" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(40,80,255,0.45)" />
        <stop offset="70%" stopColor="rgba(40,80,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="sg-l" cx="130" cy="100" rx="200" ry="120" fill="url(#sg1)" />
    <ellipse id="sg-c" cx="400" cy="110" rx="180" ry="110" fill="url(#sg2)" />
    <ellipse id="sg-r" cx="670" cy="100" rx="200" ry="120" fill="url(#sg3)" />
  </svg>

  {[
    { value: (github.user.public_repos || '–'),    label: 'REPOS',     color: '#a78bfa' },
    { value: (github.user.followers_count || '–'), label: 'FOLLOWERS', color: '#D4FF00' },
    { value: (github.user.public_gists || '–'),    label: 'GISTS',     color: '#60a5fa' },
  ].map(function(stat, i) {
    return (
      <div key={i} style={{
        display:'flex', flexDirection:'column', alignItems:'center', justifyContent:'center',
        flex:1, borderRight: i < 2 ? '1px solid rgba(255,255,255,0.07)' : 'none',
      }}>
        <div style={{ display:'flex', fontSize:40, fontWeight:800, color:stat.color, letterSpacing:'-1px', lineHeight:1 }}>
          {stat.value}
        </div>
        <div style={{ display:'flex', fontSize:11, fontWeight:600, color:'rgba(160,155,200,0.7)', letterSpacing:'2px', marginTop:6 }}>
          {stat.label}
        </div>
      </div>
    );
  })}

</div>
```

```aura width=800 height=260
<div style={{
  width:'100%', height:'100%', background:'#08080c',
  display:'flex', flexDirection:'column', justifyContent:'center',
  fontFamily:'Inter', position:'relative', overflow:'hidden',
  borderRadius:16, border:'1px solid rgba(110,80,220,0.18)',
  padding:'0 40px',
}}>

  <style>{`
    @keyframes ts-drift { 0%,100%{transform:translateX(0);opacity:0.5} 50%{transform:translateX(200px);opacity:0.8} }
    #ts-bg { animation: ts-drift 14s ease-in-out infinite; }
  `}</style>

  <svg width="800" height="260" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="tg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(110,20,210,0.40)" />
        <stop offset="70%" stopColor="rgba(110,20,210,0)" />
      </radialGradient>
    </defs>
    <ellipse id="ts-bg" cx="100" cy="200" rx="320" ry="200" fill="url(#tg1)" />
  </svg>

  <div style={{ display:'flex', fontSize:11, fontWeight:700, color:'rgba(160,155,200,0.55)', letterSpacing:'3px', marginBottom:18 }}>
    TECH STACK
  </div>

  {[
    {
      label: 'LANGUAGES',
      tags:  ['Python', 'TypeScript', 'JavaScript', 'Java'],
      color: 'rgba(212,255,0,0.88)',
      bg:    'rgba(80,60,10,0.25)',
      border:'rgba(212,255,0,0.28)',
    },
    {
      label: 'FRONTEND',
      tags:  ['React', 'Next.js', 'Tailwind CSS', 'HTML', 'CSS'],
      color: 'rgba(147,210,255,0.9)',
      bg:    'rgba(20,50,100,0.25)',
      border:'rgba(80,140,255,0.28)',
    },
    {
      label: 'BACKEND & DB',
      tags:  ['PostgreSQL', 'MongoDB', 'MySQL', 'Prisma', 'Zod'],
      color: 'rgba(180,160,255,0.9)',
      bg:    'rgba(60,30,130,0.22)',
      border:'rgba(120,80,240,0.28)',
    },
    {
      label: 'TOOLS & AI',
      tags:  ['Docker', 'Git', 'Linux', 'Vercel', 'Ollama', 'OpenRouter', 'Claude Code'],
      color: 'rgba(160,230,200,0.9)',
      bg:    'rgba(10,60,40,0.22)',
      border:'rgba(50,180,120,0.28)',
    },
  ].map(function(row) {
    return (
      <div key={row.label} style={{ display:'flex', alignItems:'center', gap:10, marginBottom:10 }}>
        <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(140,130,185,0.65)', letterSpacing:'1.5px', width:96, flexShrink:0 }}>
          {row.label}
        </div>
        <div style={{ display:'flex', gap:6, flexWrap:'wrap' }}>
          {row.tags.map(function(tag) {
            return (
              <div key={tag} style={{
                display:'flex', padding:'3px 10px', borderRadius:16,
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

## `> whoami`

```python
class NihalSheikh:
    pronouns     = "he/him"
    location     = "Nagpur, India 🇮🇳"
    education    = "B.E. Computer Engineering — G.H. Raisoni, Pune (2024)"
    currently    = ["Building SnippetVault 🗂️", "Open to full-time & freelance roles 🚀"]
    interests    = ["Full-Stack Dev", "Systems Programming", "Local LLMs", "Open Source"]
    fun_fact     = "Daily-drives Ubuntu + Hackintosh on an ASUS TUF. Hostname: aincrad."
    fueled_by    = "Chai and compiler errors ☕"
```

---

## `> cat stats.json`

<div align="center">

| ![GitHub Stats](https://github-readme-stats.vercel.app/api?username=nihalsheikh&show_icons=true&theme=gotham&hide_border=true&include_all_commits=true&count_private=true&title_color=D4FF00&icon_color=D4FF00&text_color=ffffff&bg_color=0d1117) | ![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=nihalsheikh&theme=gotham&hide_border=true&layout=compact&title_color=D4FF00&text_color=ffffff&bg_color=0d1117) |
| :-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |

<br/>

![GitHub Streak](https://streak-stats.demolab.com/?user=nihalsheikh&theme=dark&hide_border=true&ring=D4FF00&fire=D4FF00&currStreakLabel=D4FF00&background=0d1117&stroke=30363d&sideLabels=ffffff&dates=888888)

</div>

---

```aura width=150 height=44 link="https://x.com/sshNihal" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  fontFamily:'Inter', borderRadius:22, background:'#0f0f0f',
  border:'1px solid rgba(29,161,242,0.5)',
}}>
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'#e0e0e0' }}>Twitter / X</div>
</div>
```

```aura width=130 height=44 link="https://www.linkedin.com/in/nihalsheikh/" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  fontFamily:'Inter', borderRadius:22, background:'#0f0f0f',
  border:'1px solid rgba(10,102,194,0.5)',
}}>
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'#e0e0e0' }}>LinkedIn</div>
</div>
```

```aura width=130 height=44 link="https://flowcv.me/nihalsheikh" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  fontFamily:'Inter', borderRadius:22, background:'#0f0f0f',
  border:'1px solid rgba(212,255,0,0.5)',
}}>
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'#D4FF00' }}>Portfolio</div>
</div>
```

```aura width=110 height=44 link="mailto:nihalsheikh585@gmail.com" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  fontFamily:'Inter', borderRadius:22, background:'#0f0f0f',
  border:'1px solid rgba(234,67,53,0.5)',
}}>
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'#e0e0e0' }}>Gmail</div>
</div>
```

<br>
<p align="center"><sub>built with <a href="https://github.com/collectioneur/readme-aura">readme-aura</a> · nihalsheikh</sub></p>
