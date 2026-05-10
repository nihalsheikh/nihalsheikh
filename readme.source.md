```aura width=800 height=240
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

  <svg width="860" height="240" style={{ position:'absolute', top:0, left:0 }}>
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
        <stop offset="0%"  stopColor="rgba(110,80,255,0.38)" />
        <stop offset="45%" stopColor="rgba(90,60,220,0.14)" />
        <stop offset="70%" stopColor="rgba(90,60,220,0)" />
      </radialGradient>
      <radialGradient id="rg5" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(160,30,255,0.52)" />
        <stop offset="45%" stopColor="rgba(130,20,220,0.20)" />
        <stop offset="70%" stopColor="rgba(130,20,220,0)" />
      </radialGradient>
      <radialGradient id="rg6" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(80,60,255,0.30)" />
        <stop offset="70%" stopColor="rgba(80,60,255,0)" />
      </radialGradient>
      <radialGradient id="rg7" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(20,60,255,0.38)" />
        <stop offset="70%" stopColor="rgba(20,60,255,0)" />
      </radialGradient>
    </defs>
    <ellipse id="gh-1" cx="160" cy="240" rx="270" ry="220" fill="url(#rg1)" />
    <ellipse id="gh-2" cx="310" cy="250" rx="220" ry="180" fill="url(#rg2)" />
    <ellipse id="gh-3" cx="430" cy="250" rx="185" ry="160" fill="url(#rg3)" />
    <ellipse id="gh-4" cx="560" cy="255" rx="160" ry="145" fill="url(#rg4)" />
    <ellipse id="gh-5" cx="730" cy="250" rx="140" ry="130" fill="url(#rg5)" />
    <ellipse id="gh-6" cx="290" cy="245" rx="185" ry="160" fill="url(#rg6)" />
    <ellipse id="gh-7" cx="500" cy="240" rx="210" ry="185" fill="url(#rg7)" />
  </svg>

  <div style={{
    position:'absolute', left:40, top:0, bottom:0,
    display:'flex', alignItems:'center', justifyContent:'center',
  }}>
    <div style={{
      width:104, height:104, borderRadius:52,
      background:'linear-gradient(135deg, #6622ee 0%, #4466ff 100%)',
      display:'flex', alignItems:'center', justifyContent:'center',
    }}>
      <img src={github.user.avatarUrl} width={96} height={96} style={{ borderRadius:48 }} />
    </div>
  </div>

  <div style={{ display:'flex', flexDirection:'column', marginLeft:168, gap:8, paddingRight:32 }}>

    <div style={{ display:'flex', fontSize:34, fontWeight:800, color:'#ffffff', letterSpacing:'-0.5px', lineHeight:1 }}>
      {github.user.name || 'Nihal Sheikh'}
    </div>

    <div style={{ display:'flex', fontSize:13, color:'rgba(180,170,255,0.80)', fontWeight:400 }}>
      Full-Stack Developer · Open Source Builder · AI Tinkerer
    </div>

    <div style={{ display:'flex', gap:20, fontSize:12, color:'rgba(140,130,190,0.70)', fontWeight:500 }}>
      <div style={{ display:'flex' }}>📍 India</div>
    </div>

    <div style={{ display:'flex', fontSize:12, color:'rgba(160,200,255,0.75)', fontWeight:500 }}>
      🔨 Building SnippetVault &nbsp;·&nbsp; 🚀 Open to full-time &amp; freelance
    </div>

    <div style={{ display:'flex', gap:7, marginTop:2 }}>
      {['Python', 'TypeScript', 'Next.js', 'React'].map(function(tag) {
        return (
          <div key={tag} style={{
            display:'flex', padding:'3px 12px', borderRadius:20,
            background:'rgba(80,40,220,0.22)', border:'1px solid rgba(110,80,240,0.38)',
            color:'rgba(200,190,255,0.92)', fontSize:11, fontWeight:700,
          }}>{tag}</div>
        );
      })}
    </div>

  </div>

</div>
```

```aura width=800 height=260
<div style={{
  width:'100%', height:'100%', background:'#08080c',
  display:'flex', flexDirection:'column', justifyContent:'center',
  fontFamily:'Inter', position:'relative', overflow:'hidden',
  borderRadius:16, border:'1px solid rgba(80,60,200,0.18)',
  padding:'0 40px',
}}>

  <style>{`
    @keyframes ts-drift { 0%,100%{transform:translateX(0);opacity:0.4} 50%{transform:translateX(220px);opacity:0.7} }
    #ts-bg { animation: ts-drift 16s ease-in-out infinite; }
  `}</style>

  <svg width="800" height="260" style={{ position:'absolute', top:0, left:0 }}>
    <defs>
      <radialGradient id="tg1" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(90,20,200,0.38)" />
        <stop offset="70%" stopColor="rgba(90,20,200,0)" />
      </radialGradient>
    </defs>
    <ellipse id="ts-bg" cx="80" cy="210" rx="300" ry="190" fill="url(#tg1)" />
  </svg>

  <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(140,130,185,0.45)', letterSpacing:'3px', marginBottom:16 }}>
    TECH STACK
  </div>

  {[
    {
      label: 'LANGUAGES',
      tags:  ['Python', 'TypeScript', 'JavaScript', 'Java'],
      color: 'rgba(255,200,100,0.90)',
      bg:    'rgba(60,40,0,0.30)',
      border:'rgba(200,140,20,0.30)',
    },
    {
      label: 'FRONTEND',
      tags:  ['React', 'Next.js', 'Tailwind CSS', 'HTML', 'CSS'],
      color: 'rgba(120,200,255,0.92)',
      bg:    'rgba(10,40,90,0.30)',
      border:'rgba(40,120,255,0.30)',
    },
    {
      label: 'BACKEND & DB',
      tags:  ['PostgreSQL', 'MongoDB', 'MySQL', 'Prisma', 'Zod'],
      color: 'rgba(170,140,255,0.92)',
      bg:    'rgba(50,20,120,0.28)',
      border:'rgba(100,60,240,0.30)',
    },
    {
      label: 'TOOLS & AI',
      tags:  ['Docker', 'Git', 'Linux', 'Vercel', 'Ollama', 'OpenRouter', 'Claude Code'],
      color: 'rgba(100,220,180,0.92)',
      bg:    'rgba(0,50,35,0.28)',
      border:'rgba(30,160,110,0.30)',
    },
  ].map(function(row) {
    return (
      <div key={row.label} style={{ display:'flex', alignItems:'center', gap:10, marginBottom:10 }}>
        <div style={{ display:'flex', fontSize:10, fontWeight:700, color:'rgba(120,110,170,0.55)', letterSpacing:'1.5px', width:90, flexShrink:0 }}>
          {row.label}
        </div>
        <div style={{ display:'flex', gap:6, flexWrap:'wrap' }}>
          {row.tags.map(function(tag) {
            return (
              <div key={tag} style={{
                display:'flex', padding:'3px 10px', borderRadius:14,
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

```aura width=138 height=44 link="https://x.com/sshNihal" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  gap:7, fontFamily:'Inter', borderRadius:22, background:'#0d0d0d',
  border:'1px solid rgba(29,161,242,0.45)',
}}>
  <img src="./icons/x.svg" width={14} height={14} />
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'rgba(29,161,242,0.90)' }}>Twitter / X</div>
</div>
```

```aura width=120 height=44 link="https://www.linkedin.com/in/nihalsheikh/" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  gap:7, fontFamily:'Inter', borderRadius:22, background:'#0d0d0d',
  border:'1px solid rgba(80,130,255,0.45)',
}}>
  <img src="./icons/linkedin.svg" width={14} height={14} />
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'rgba(100,155,255,0.90)' }}>LinkedIn</div>
</div>
```

```aura width=128 height=44 link="https://flowcv.me/nihalsheikh" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  gap:7, fontFamily:'Inter', borderRadius:22, background:'#0d0d0d',
  border:'1px solid rgba(130,100,255,0.45)',
}}>
  <img src="./icons/globe.svg" width={14} height={14} />
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'rgba(160,140,255,0.90)' }}>Portfolio</div>
</div>
```

```aura width=106 height=44 link="mailto:nihalsheikh585@gmail.com" inline align=center
<div style={{
  width:'100%', height:'100%', display:'flex', alignItems:'center', justifyContent:'center',
  gap:7, fontFamily:'Inter', borderRadius:22, background:'#0d0d0d',
  border:'1px solid rgba(234,67,53,0.45)',
}}>
  <img src="./icons/gmail.svg" width={14} height={14} />
  <div style={{ display:'flex', fontSize:13, fontWeight:600, color:'rgba(255,110,90,0.90)' }}>Gmail</div>
</div>
```

<br>
<p align="center"><sub>powered by <a href="https://github.com/collectioneur/readme-aura">readme-aura</a> · nihalsheikh</sub></p>
