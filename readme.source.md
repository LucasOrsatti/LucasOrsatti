<!--
  ATENCAO: este README e GERADO. Nao edite README.md.
  Edite este arquivo (readme.source.md) e rode: npx readme-aura build -g Guilherme-lima-18
  Qualquer alteracao feita no README.md e perdida no proximo build.
-->

```aura width=880 height=300 link="https://github.com/Guilherme-lima-18"
<div style={{
  width: '100%', height: '100%', background: '#0a0506',
  display: 'flex', flexDirection: 'column', fontFamily: 'Inter',
  position: 'relative', overflow: 'hidden', borderRadius: 14,
  border: '1px solid rgba(255,77,77,0.24)',
}}>

  <style>{`
      @keyframes drift-a {
        0%, 100% { transform: translateX(-40px); opacity: 0.75; }
        50%      { transform: translateX(320px); opacity: 1; }
      }
      @keyframes drift-b {
        0%, 100% { transform: translateX(60px);  opacity: 0.55; }
        50%      { transform: translateX(-240px); opacity: 0.95; }
      }
      @keyframes drift-c {
        0%, 100% { transform: translateX(0px);   opacity: 0.8; }
        33%      { transform: translateX(180px); opacity: 0.5; }
        66%      { transform: translateX(-120px); opacity: 1; }
      }
      @keyframes drift-d {
        0%, 100% { transform: translateX(0px);   opacity: 0.45; }
        50%      { transform: translateX(260px); opacity: 0.9; }
      }
      @keyframes scan {
        0%   { transform: translateY(-10px); opacity: 0; }
        12%  { opacity: 0.55; }
        88%  { opacity: 0.55; }
        100% { transform: translateY(300px); opacity: 0; }
      }
      @keyframes blink {
        0%, 48%   { opacity: 1; }
        49%, 100% { opacity: 0; }
      }
      #aura-a { animation: drift-a 11s ease-in-out infinite; }
      #aura-b { animation: drift-b 14s ease-in-out infinite; }
      #aura-c { animation: drift-c 9s  ease-in-out infinite; }
      #aura-d { animation: drift-d 13s ease-in-out infinite; }
      #scanline { animation: scan 6s linear infinite; }
      #caret { animation: blink 1.1s step-end infinite; }
    `}</style>

  <svg width="880" height="300" style={{ position: 'absolute', top: 0, left: 0 }}>
    <defs>
      <radialGradient id="ra" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(255,59,59,0.42)" />
        <stop offset="45%" stopColor="rgba(184,27,42,0.18)" />
        <stop offset="72%" stopColor="rgba(184,27,42,0)" />
      </radialGradient>
      <radialGradient id="rb" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(224,36,52,0.36)" />
        <stop offset="50%" stopColor="rgba(142,20,32,0.16)" />
        <stop offset="74%" stopColor="rgba(142,20,32,0)" />
      </radialGradient>
      <radialGradient id="rc" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(255,138,138,0.24)" />
        <stop offset="70%" stopColor="rgba(255,138,138,0)" />
      </radialGradient>
      <radialGradient id="rd" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="rgba(100,14,23,0.55)" />
        <stop offset="55%" stopColor="rgba(100,14,23,0.20)" />
        <stop offset="76%" stopColor="rgba(100,14,23,0)" />
      </radialGradient>
      <linearGradient id="sheen" x1="0" y1="0" x2="1" y2="1">
        <stop offset="0%"   stopColor="rgba(255,255,255,0.05)" />
        <stop offset="45%"  stopColor="rgba(255,255,255,0.01)" />
        <stop offset="100%" stopColor="rgba(0,0,0,0.34)" />
      </linearGradient>
      <linearGradient id="scanfade" x1="0" y1="0" x2="1" y2="0">
        <stop offset="0%"   stopColor="rgba(255,77,77,0)" />
        <stop offset="30%"  stopColor="rgba(255,90,90,0.30)" />
        <stop offset="70%"  stopColor="rgba(255,90,90,0.30)" />
        <stop offset="100%" stopColor="rgba(255,77,77,0)" />
      </linearGradient>
      <filter id="grain" x="0" y="0" width="100%" height="100%">
        <feTurbulence type="fractalNoise" baseFrequency="0.9" numOctaves="2" stitchTiles="stitch" result="noise" />
        <feColorMatrix type="saturate" values="0" />
      </filter>
      <radialGradient id="edge" cx="50%" cy="50%" r="50%">
        <stop offset="0%"  stopColor="#000000" />
        <stop offset="42%" stopColor="#000000" />
        <stop offset="63%" stopColor="#ffffff" />
        <stop offset="82%" stopColor="#000000" />
      </radialGradient>
      <mask id="grain-edge">
        <ellipse cx="340" cy="250" rx="420" ry="280" fill="url(#edge)" />
      </mask>
    </defs>

    <ellipse id="aura-a" cx="150" cy="260" rx="280" ry="180" fill="url(#ra)" />
    <ellipse id="aura-b" cx="420" cy="285" rx="240" ry="165" fill="url(#rb)" />
    <ellipse id="aura-c" cx="640" cy="270" rx="200" ry="150" fill="url(#rc)" />
    <ellipse id="aura-d" cx="300" cy="295" rx="330" ry="200" fill="url(#rd)" />

    <rect x="0" y="0" width="880" height="300" fill="url(#sheen)" />
    <g mask="url(#grain-edge)">
      <rect x="0" y="0" width="880" height="300" filter="url(#grain)" opacity="0.15" />
    </g>

    <rect id="scanline" x="0" y="0" width="880" height="2" fill="url(#scanfade)" />
    <rect id="caret" x="49" y="238" width="9" height="17" fill="#FF3B3B" rx="1" />
  </svg>

  <div style={{
    display: 'flex', flexDirection: 'row', alignItems: 'center',
    height: 40, paddingLeft: 16, paddingRight: 16, gap: 8,
    borderBottom: '1px solid rgba(255,77,77,0.20)',
    background: 'rgba(255,59,59,0.05)',
  }}>
    <div style={{ display: 'flex', width: 10, height: 10, borderRadius: 5, background: '#FF5C5C' }} />
    <div style={{ display: 'flex', width: 10, height: 10, borderRadius: 5, background: '#B81B2A' }} />
    <div style={{ display: 'flex', width: 10, height: 10, borderRadius: 5, background: '#640E17' }} />
    <div style={{
      display: 'flex', marginLeft: 14, fontSize: 12, fontWeight: 700,
      color: 'rgba(255,190,190,0.68)', letterSpacing: '1.4px',
    }}>
      sirusfruit@github : ~/profile
    </div>
    <div style={{ display: 'flex', flexGrow: 1 }} />
    <div style={{
      display: 'flex', fontSize: 11, fontWeight: 700,
      color: 'rgba(255,140,140,0.55)', letterSpacing: '1.4px',
    }}>
      zsh
    </div>
  </div>

  <div style={{
    display: 'flex', flexDirection: 'row', flexGrow: 1,
    paddingLeft: 30, paddingRight: 30, paddingTop: 22, paddingBottom: 22,
  }}>

    <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 7 }}>

      <div style={{ display: 'flex', flexDirection: 'row', alignItems: 'center', gap: 8 }}>
        <div style={{ display: 'flex', fontSize: 14, fontWeight: 700, color: '#FF3B3B' }}>$</div>
        <div style={{ display: 'flex', fontSize: 14, color: 'rgba(255,190,190,0.60)', letterSpacing: '0.6px' }}>whoami</div>
      </div>

      <div style={{
        display: 'flex', fontSize: 42, fontWeight: 700, color: '#ffffff',
        letterSpacing: '-1.4px', lineHeight: 1.05,
      }}>
        SirusFruit
      </div>

      <div style={{
        display: 'flex', fontSize: 15, fontWeight: 700,
        color: 'rgba(255,150,150,0.90)', letterSpacing: '0.4px',
      }}>
        Software Engineer
      </div>

      <div style={{ display: 'flex', flexDirection: 'row', alignItems: 'center', gap: 8, marginTop: 10 }}>
        <div style={{ display: 'flex', fontSize: 14, fontWeight: 700, color: '#FF3B3B' }}>$</div>
        <div style={{ display: 'flex', fontSize: 14, color: 'rgba(255,190,190,0.60)', letterSpacing: '0.6px' }}>tags --list</div>
      </div>

      <div style={{ display: 'flex', flexDirection: 'row', gap: 7, flexWrap: 'wrap', marginTop: 2 }}>
        {['java', 'go', 'aws', 'spring', 'linux'].map(function (tag, i) {
          return (
            <div key={tag + '-' + i} style={{
              display: 'flex', flexDirection: 'row', alignItems: 'center', gap: 6,
              paddingLeft: 10, paddingRight: 10, paddingTop: 4, paddingBottom: 4,
              borderRadius: 5, background: 'rgba(255,59,59,0.09)',
              border: '1px solid rgba(255,77,77,0.34)',
            }}>
              <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(255,120,120,0.75)' }}>#</div>
              <div style={{ display: 'flex', fontSize: 12, fontWeight: 700, color: 'rgba(255,224,224,0.94)' }}>{tag}</div>
            </div>
          );
        })}
      </div>

      <div style={{ display: 'flex', flexDirection: 'row', alignItems: 'center', gap: 8, marginTop: 8 }}>
        <div style={{ display: 'flex', width: 230, fontSize: 14, fontWeight: 700, color: '#FF3B3B' }}>$</div>
      </div>

    </div>

    <div style={{
      display: 'flex', width: 132, height: 132, position: 'relative',
      alignItems: 'center', justifyContent: 'center', marginTop: 8,
    }}>
      <div style={{
        display: 'flex', position: 'absolute', top: 0, left: 0, width: 132, height: 132,
        borderRadius: 10, border: '1px solid rgba(255,77,77,0.45)',
        background: 'linear-gradient(135deg, rgba(255,59,59,0.20), rgba(100,14,23,0.35))',
      }} />
      <div style={{ display: 'flex', position: 'absolute', top: -1, left: -1, width: 16, height: 2, background: '#FF3B3B' }} />
      <div style={{ display: 'flex', position: 'absolute', top: -1, left: -1, width: 2, height: 16, background: '#FF3B3B' }} />
      <div style={{ display: 'flex', position: 'absolute', bottom: -1, right: -1, width: 16, height: 2, background: '#FF3B3B' }} />
      <div style={{ display: 'flex', position: 'absolute', bottom: -1, right: -1, width: 2, height: 16, background: '#FF3B3B' }} />
      <img src=".github/img/avatar.png" width={112} height={112} style={{ borderRadius: 6 }} />
    </div>

  </div>
</div>
```

<p align="center">
I build things, break them, and rebuild them better.<br />
Most of what I know started as a bug I refused to ignore.
</p>

```aura width=880 height=338
<div style={{
  width: '100%', height: '100%', background: '#0a0506',
  display: 'flex', flexDirection: 'column', fontFamily: 'Inter',
  borderRadius: 14, border: '1px solid rgba(255,77,77,0.24)',
  overflow: 'hidden',
}}>

  <div style={{
    display: 'flex', flexDirection: 'row', alignItems: 'center',
    height: 38, paddingLeft: 16, paddingRight: 16, gap: 8,
    borderBottom: '1px solid rgba(255,77,77,0.20)',
    background: 'rgba(255,59,59,0.05)',
  }}>
    <div style={{ display: 'flex', width: 9, height: 9, borderRadius: 5, background: '#FF5C5C' }} />
    <div style={{ display: 'flex', width: 9, height: 9, borderRadius: 5, background: '#B81B2A' }} />
    <div style={{ display: 'flex', width: 9, height: 9, borderRadius: 5, background: '#640E17' }} />
    <div style={{
      display: 'flex', marginLeft: 14, fontSize: 12, fontWeight: 700,
      color: 'rgba(255,190,190,0.68)', letterSpacing: '1.4px',
    }}>
      tree ~/stack
    </div>
  </div>

  <div style={{
    display: 'flex', flexDirection: 'column', position: 'relative', flexGrow: 1,
    paddingLeft: 28, paddingRight: 28, paddingTop: 18, paddingBottom: 18,
  }}>

    <div style={{
      display: 'flex', position: 'absolute', left: 34, top: 44, width: 1, height: 208,
      background: 'rgba(255,77,77,0.30)',
    }} />

    {[
      { dir: 'languages',  items: [['Java', '#FF3B3B'], ['Go', '#F03242'], ['TypeScript', '#E02434'], ['C#', '#C71F2E'], ['Python', '#A81828'], ['C', '#8E1420']] },
      { dir: 'frameworks', items: [['Spring', '#FF3B3B'], ['Maven', '#E02434']] },
      { dir: 'web',        items: [['HTML', '#FF3B3B'], ['CSS', '#E02434']] },
      { dir: 'databases',  items: [['PostgreSQL', '#FF3B3B'], ['MySQL', '#E02434']] },
      { dir: 'infra',      items: [['AWS', '#FF3B3B'], ['Linux', '#E02434'], ['Fedora', '#C71F2E']] },
    ].map(function (row, r, all) {
      return (
        <div key={row.dir} style={{
          display: 'flex', flexDirection: 'row', alignItems: 'center',
          height: 52, gap: 10,
        }}>
          <div style={{ display: 'flex', width: 6, height: 1 }} />
          <div style={{ display: 'flex', width: 16, height: 1, background: 'rgba(255,77,77,0.30)' }} />
          <div style={{
            display: 'flex', width: 104, fontSize: 12, fontWeight: 700,
            color: 'rgba(255,150,150,0.82)', letterSpacing: '0.2px',
          }}>
            {row.dir}/
          </div>
          <div style={{ display: 'flex', flexDirection: 'row', gap: 7, flexWrap: 'wrap' }}>
            {row.items.map(function (it, i) {
              return (
                <div key={it[0]} style={{
                  display: 'flex', flexDirection: 'row', alignItems: 'center', gap: 7,
                  paddingLeft: 10, paddingRight: 11, paddingTop: 5, paddingBottom: 5,
                  borderRadius: 5, background: 'rgba(255,59,59,0.06)',
                  border: '1px solid rgba(255,77,77,0.26)',
                }}>
                  <div style={{ display: 'flex', width: 3, height: 12, borderRadius: 2, background: it[1] }} />
                  <div style={{ display: 'flex', fontSize: 12, fontWeight: 700, color: 'rgba(255,232,232,0.93)' }}>{it[0]}</div>
                </div>
              );
            })}
          </div>
        </div>
      );
    })}

  </div>
</div>
```

```aura width=880 height=356
<div style={{
  width: '100%', height: '100%', background: '#0a0506',
  display: 'flex', flexDirection: 'column', fontFamily: 'Inter',
  borderRadius: 14, border: '1px solid rgba(255,77,77,0.24)',
  overflow: 'hidden',
}}>

  <div style={{
    display: 'flex', flexDirection: 'row', alignItems: 'center',
    height: 38, paddingLeft: 16, paddingRight: 16, gap: 8,
    borderBottom: '1px solid rgba(255,77,77,0.20)',
    background: 'rgba(255,59,59,0.05)',
  }}>
    <div style={{ display: 'flex', width: 9, height: 9, borderRadius: 5, background: '#FF5C5C' }} />
    <div style={{ display: 'flex', width: 9, height: 9, borderRadius: 5, background: '#B81B2A' }} />
    <div style={{ display: 'flex', width: 9, height: 9, borderRadius: 5, background: '#640E17' }} />
    <div style={{
      display: 'flex', marginLeft: 14, fontSize: 12, fontWeight: 700,
      color: 'rgba(255,190,190,0.68)', letterSpacing: '1.4px',
    }}>
      gh stats --graph
    </div>
  </div>

  <div style={{
    display: 'flex', flexDirection: 'column', flexGrow: 1,
    paddingLeft: 28, paddingRight: 28, paddingTop: 18, paddingBottom: 18, gap: 16,
  }}>

    <div style={{ display: 'flex', flexDirection: 'row', gap: 10 }}>
      {[
        ['repos',     github?.stats?.totalRepos   ?? 0],
        ['commits',   github?.stats?.totalCommits ?? 0],
        ['followers', github?.user?.followers     ?? 0],
        ['langs',     (github?.languages ?? []).length],
      ].map(function (s, i) {
        return (
          <div key={s[0]} style={{
            display: 'flex', flexDirection: 'column', width: 196, gap: 2,
            paddingLeft: 14, paddingRight: 14, paddingTop: 10, paddingBottom: 10,
            borderRadius: 8, background: 'rgba(255,59,59,0.06)',
            border: '1px solid rgba(255,77,77,0.26)',
          }}>
            <div style={{
              display: 'flex', fontSize: 26, fontWeight: 700,
              color: '#ffffff', letterSpacing: '-0.8px', lineHeight: 1.1,
            }}>
              {String(s[1])}
            </div>
            <div style={{
              display: 'flex', fontSize: 11, fontWeight: 700,
              color: 'rgba(255,150,150,0.72)', letterSpacing: '1.2px',
            }}>
              {s[0]}
            </div>
          </div>
        );
      })}
    </div>

    <div style={{ display: 'flex', flexDirection: 'column', gap: 7 }}>
      <div style={{
        display: 'flex', fontSize: 11, fontWeight: 700,
        color: 'rgba(255,150,150,0.62)', letterSpacing: '1.6px', marginBottom: 2,
      }}>
        LANGUAGE DISTRIBUTION
      </div>

      {(function () {
        var langs = (github?.languages ?? []).slice(0, 6);
        var ramp = ['#FF3B3B', '#F03242', '#E02434', '#C71F2E', '#A81828', '#8E1420'];
        var max = 1;
        for (var k = 0; k < langs.length; k++) {
          if (langs[k].percentage > max) max = langs[k].percentage;
        }
        return langs.map(function (l, i) {
          var w = Math.max(6, Math.round((l.percentage / max) * 476));
          return (
            <div key={l.name} style={{ display: 'flex', flexDirection: 'row', alignItems: 'center', height: 24, gap: 12 }}>
              <div style={{
                display: 'flex', width: 96, fontSize: 12, fontWeight: 700,
                color: 'rgba(255,232,232,0.92)',
              }}>
                {l.name}
              </div>
              <div style={{
                display: 'flex', width: 476, height: 10, borderRadius: 5,
                background: 'rgba(255,77,77,0.10)',
              }}>
                <div style={{ display: 'flex', width: w, height: 10, borderRadius: 5, background: ramp[i % 6] }} />
              </div>
              <div style={{
                display: 'flex', width: 46, fontSize: 12, fontWeight: 700,
                color: 'rgba(255,150,150,0.82)', justifyContent: 'flex-end',
              }}>
                {l.percentage + '%'}
              </div>
            </div>
          );
        });
      })()}
    </div>

  </div>
</div>
```

```aura width=880 height=46
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 10,
  border: '1px solid rgba(255,77,77,0.24)', paddingLeft: 18, paddingRight: 18, gap: 9,
}}>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>$</div>
  <div style={{ display: 'flex', fontSize: 13, color: 'rgba(255,190,190,0.62)', letterSpacing: '0.6px' }}>ls ~/projects</div>
  <div style={{ display: 'flex', flexGrow: 1 }} />
  <div style={{ display: 'flex', fontSize: 11, fontWeight: 700, color: 'rgba(255,140,140,0.50)', letterSpacing: '1.2px' }}>6 selected</div>
</div>
```

```aura width=432 height=66 link="https://github.com/Guilherme-lima-18/RPG-Go" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.26)',
  paddingLeft: 14, paddingRight: 14, gap: 11,
}}>
  <div style={{ display: 'flex', width: 3, height: 38, borderRadius: 2, background: '#FF3B3B' }} />
  <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 4 }}>
    <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: 'rgba(255,240,240,0.95)' }}>RPG Go</div>
    <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255,175,175,0.62)' }}>A simple RPG built in Go for practice</div>
  </div>
  <div style={{
    display: 'flex', alignItems: 'center', paddingLeft: 9, paddingRight: 9, paddingTop: 4, paddingBottom: 4,
    borderRadius: 5, background: 'rgba(255,59,59,0.08)', border: '1px solid rgba(255,77,77,0.28)',
    fontSize: 10, fontWeight: 700, color: '#FF3B3B',
  }}>Go</div>
</div>
```

```aura width=432 height=66 link="https://github.com/Guilherme-lima-18/ProjetoMassager" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.26)',
  paddingLeft: 14, paddingRight: 14, gap: 11,
}}>
  <div style={{ display: 'flex', width: 3, height: 38, borderRadius: 2, background: '#F03242' }} />
  <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 4 }}>
    <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: 'rgba(255,240,240,0.95)' }}>ProjetoMassager</div>
    <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255,175,175,0.62)' }}>Full-stack application in TypeScript</div>
  </div>
  <div style={{
    display: 'flex', alignItems: 'center', paddingLeft: 9, paddingRight: 9, paddingTop: 4, paddingBottom: 4,
    borderRadius: 5, background: 'rgba(255,59,59,0.08)', border: '1px solid rgba(255,77,77,0.28)',
    fontSize: 10, fontWeight: 700, color: '#F03242',
  }}>TypeScript</div>
</div>
```

```aura width=432 height=66 link="https://github.com/Guilherme-lima-18/-Java-Banking-System" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.26)',
  paddingLeft: 14, paddingRight: 14, gap: 11,
}}>
  <div style={{ display: 'flex', width: 3, height: 38, borderRadius: 2, background: '#E02434' }} />
  <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 4 }}>
    <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: 'rgba(255,240,240,0.95)' }}>Java Banking System</div>
    <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255,175,175,0.62)' }}>Deposit, withdrawal and balance simulation</div>
  </div>
  <div style={{
    display: 'flex', alignItems: 'center', paddingLeft: 9, paddingRight: 9, paddingTop: 4, paddingBottom: 4,
    borderRadius: 5, background: 'rgba(255,59,59,0.08)', border: '1px solid rgba(255,77,77,0.28)',
    fontSize: 10, fontWeight: 700, color: '#E02434',
  }}>Java</div>
</div>
```

```aura width=432 height=66 link="https://github.com/Guilherme-lima-18/Java-OOP-Project---Vehicle-System" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.26)',
  paddingLeft: 14, paddingRight: 14, gap: 11,
}}>
  <div style={{ display: 'flex', width: 3, height: 38, borderRadius: 2, background: '#E02434' }} />
  <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 4 }}>
    <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: 'rgba(255,240,240,0.95)' }}>Java OOP Project — Vehicle System</div>
    <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255,175,175,0.62)' }}>OOP modeling of a vehicle system</div>
  </div>
  <div style={{
    display: 'flex', alignItems: 'center', paddingLeft: 9, paddingRight: 9, paddingTop: 4, paddingBottom: 4,
    borderRadius: 5, background: 'rgba(255,59,59,0.08)', border: '1px solid rgba(255,77,77,0.28)',
    fontSize: 10, fontWeight: 700, color: '#E02434',
  }}>Java</div>
</div>
```

```aura width=432 height=66 link="https://github.com/Guilherme-lima-18/Java-Anotation-System" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.26)',
  paddingLeft: 14, paddingRight: 14, gap: 11,
}}>
  <div style={{ display: 'flex', width: 3, height: 38, borderRadius: 2, background: '#E02434' }} />
  <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 4 }}>
    <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: 'rgba(255,240,240,0.95)' }}>Java Anotation System</div>
    <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255,175,175,0.62)' }}>Java annotations and reflection</div>
  </div>
  <div style={{
    display: 'flex', alignItems: 'center', paddingLeft: 9, paddingRight: 9, paddingTop: 4, paddingBottom: 4,
    borderRadius: 5, background: 'rgba(255,59,59,0.08)', border: '1px solid rgba(255,77,77,0.28)',
    fontSize: 10, fontWeight: 700, color: '#E02434',
  }}>Java</div>
</div>
```

```aura width=432 height=66 link="https://github.com/Guilherme-lima-18/Projeto-Site-IA" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row', alignItems: 'center',
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.26)',
  paddingLeft: 14, paddingRight: 14, gap: 11,
}}>
  <div style={{ display: 'flex', width: 3, height: 38, borderRadius: 2, background: '#A81828' }} />
  <div style={{ display: 'flex', flexDirection: 'column', flexGrow: 1, gap: 4 }}>
    <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: 'rgba(255,240,240,0.95)' }}>Projeto Site IA</div>
    <div style={{ display: 'flex', fontSize: 10, color: 'rgba(255,175,175,0.62)' }}>AI-themed website built with HTML/CSS</div>
  </div>
  <div style={{
    display: 'flex', alignItems: 'center', paddingLeft: 9, paddingRight: 9, paddingTop: 4, paddingBottom: 4,
    borderRadius: 5, background: 'rgba(255,59,59,0.08)', border: '1px solid rgba(255,77,77,0.28)',
    fontSize: 10, fontWeight: 700, color: '#A81828',
  }}>CSS</div>
</div>
```

```aura width=880 height=52
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row',
  alignItems: 'stretch', fontFamily: 'Inter', background: '#0a0506',
  borderRadius: 10, overflow: 'hidden', border: '1px solid rgba(255,77,77,0.24)',
}}>
  {[
    { text: 'SirusFruit',   bg: '#8E1420', fg: '#ffffff',            w: 128 },
    { text: 'main',         bg: '#640E17', fg: 'rgba(255,224,224,0.92)', w: 92 },
    { text: 'building',     bg: '#40080F', fg: 'rgba(255,190,190,0.85)', w: 118 },
  ].map(function (seg, i) {
    return (
      <div key={seg.text} style={{
        display: 'flex', alignItems: 'center', justifyContent: 'center',
        width: seg.w, background: seg.bg, fontSize: 12, fontWeight: 700,
        color: seg.fg, letterSpacing: '1.2px',
      }}>
        {seg.text}
      </div>
    );
  })}

  <div style={{
    display: 'flex', flexGrow: 1, alignItems: 'center', paddingLeft: 18, gap: 9,
    background: 'rgba(255,59,59,0.04)',
  }}>
    <div style={{ display: 'flex', width: 7, height: 7, borderRadius: 4, background: '#FF3B3B' }} />
    <div style={{
      display: 'flex', fontSize: 12, fontWeight: 700,
      color: 'rgba(255,180,180,0.78)', letterSpacing: '0.8px',
    }}>
      open to collaborate
    </div>
  </div>

  <div style={{
    display: 'flex', alignItems: 'center', paddingRight: 20,
    background: 'rgba(255,59,59,0.04)',
  }}>
    <div style={{
      display: 'flex', fontSize: 12, fontWeight: 700,
      color: 'rgba(255,150,150,0.70)', letterSpacing: '0.6px',
    }}>
      github.com/Guilherme-lima-18
    </div>
  </div>
</div>
```

```aura width=210 height=44 link="https://github.com/Guilherme-lima-18" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row',
  alignItems: 'center', justifyContent: 'center', gap: 9,
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.42)',
}}>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>[</div>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#f7e6e6', letterSpacing: '0.8px' }}>github</div>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>]</div>
</div>
```

```aura width=300 height=44 link="mailto:guilhermealima70@gmail.com" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row',
  alignItems: 'center', justifyContent: 'center', gap: 9,
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.42)',
}}>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>[</div>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#f7e6e6', letterSpacing: '0.4px' }}>guilhermealima70@gmail.com</div>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>]</div>
</div>
```

```aura width=210 height=44 link="https://www.linkedin.com/in/guilherme-lima-061a36351/" inline align=center
<div style={{
  width: '100%', height: '100%', display: 'flex', flexDirection: 'row',
  alignItems: 'center', justifyContent: 'center', gap: 9,
  fontFamily: 'Inter', background: '#0a0506', borderRadius: 8,
  border: '1px solid rgba(255,77,77,0.42)',
}}>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>[</div>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#f7e6e6', letterSpacing: '0.8px' }}>linkedin</div>
  <div style={{ display: 'flex', fontSize: 13, fontWeight: 700, color: '#FF3B3B' }}>]</div>
</div>
```
