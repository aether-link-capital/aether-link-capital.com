import { useState, useEffect, useRef, useCallback, createContext, useContext } from "react";
import { AreaChart, Area, XAxis, YAxis, Tooltip, ResponsiveContainer, CartesianGrid } from "recharts";
import {
  LayoutDashboard, ArrowDownToLine, ArrowUpFromLine, List, User,
  Headphones, Copy, Check, Bell, Shield, TrendingUp,
  TrendingDown, AlertTriangle, CheckCircle2, Clock, Eye, EyeOff,
  Zap, Globe, BarChart3, ChevronDown, ArrowRight, Wallet,
  Settings, Activity, ChevronRight, Menu, X, RefreshCw,
  Star, Gem, Award, Trophy, Crown, TrendingUp as Trend,
  Sun, Moon
} from "lucide-react";

/* ── Premium Color Palette ── */
const G  = "#C9A84C";   // Gold accent
const GD = "#A07830";   // Gold dark  
const G2 = "#E8C97A";   // Gold light
const ACCENT2 = "#7C6FCD"; // Indigo
const ACCENT3 = "#4FC3F7"; // Cyan

/* ── Theme Context ── */
const ThemeCtx = createContext({ dark: true, toggle: () => {} });
const useTheme = () => useContext(ThemeCtx);

const DARK = {
  bg:       "#060914",
  bgCard:   "rgba(8,11,26,0.78)",
  bgSurf:   "rgba(5,7,18,0.92)",
  bgInput:  "rgba(8,10,25,0.80)",
  border:   "rgba(201,168,76,0.13)",
  borderSub:"rgba(120,140,200,0.12)",
  text:     "#E8EAF6",
  textSub:  "#546190",
  textMuted:"#3D4F7C",
  sidebar:  "rgba(6,8,20,0.90)",
  header:   "rgba(4,6,18,0.88)",
  ticker:   "rgba(4,6,16,0.88)",
  card:     "rgba(8,11,26,0.72)",
  infoCard: "#0E1225",
  navHover: "rgba(201,168,76,0.06)",
};

const LIGHT = {
  bg:       "#F0F2FA",
  bgCard:   "rgba(255,255,255,0.92)",
  bgSurf:   "rgba(240,242,250,0.98)",
  bgInput:  "rgba(235,237,250,0.95)",
  border:   "rgba(201,168,76,0.30)",
  borderSub:"rgba(100,120,200,0.18)",
  text:     "#0D1130",
  textSub:  "#4A5580",
  textMuted:"#8090B8",
  sidebar:  "rgba(245,246,255,0.97)",
  header:   "rgba(240,242,250,0.96)",
  ticker:   "rgba(230,233,248,0.98)",
  card:     "rgba(255,255,255,0.88)",
  infoCard: "#EEF0FC",
  navHover: "rgba(201,168,76,0.08)",
};

const CHART = [
  {d:"Dec 1",v:10200},{d:"Dec 6",v:11800},{d:"Dec 11",v:10400},
  {d:"Dec 16",v:13900},{d:"Dec 21",v:15600},{d:"Dec 26",v:13800},
  {d:"Jan 1",v:17200},{d:"Jan 6",v:15800},{d:"Jan 11",v:19400},
  {d:"Jan 16",v:17600},{d:"Jan 21",v:20800},{d:"Jan 26",v:18900},
  {d:"Jan 30",v:20100},
];

const COIN_META = {
  BTC:  {name:"Bitcoin",  clr:"#F7931A", bal:0, addr:"bc1qtjzjauzdfd349xl3xzfn7z3a4a6k3tsmc98m66",           net:"Bitcoin Network",  sym:"₿", networks:null},
  ETH:  {name:"Ethereum", clr:"#627EEA", bal:0, addr:"0x18d783350a128CABB231A8Cf30659A2c6DFCdF76",            net:"Ethereum Mainnet", sym:"Ξ", networks:null},
  USDT: {name:"Tether",   clr:"#26A17B", bal:0, addr:"0x18d783350a128CABB231A8Cf30659A2c6DFCdF76",            net:"ERC-20 (Ethereum)", sym:"₮",
    networks:[
      { label:"ERC-20", name:"Ethereum Mainnet", addr:"0x18d783350a128CABB231A8Cf30659A2c6DFCdF76", clr:"#627EEA" },
      { label:"BEP-20", name:"BNB Smart Chain",  addr:"0x18d783350a128CABB231A8Cf30659A2c6DFCdF76", clr:"#F3BA2F" },
    ]
  },
};

const TICK_META = ["BTC","ETH","BNB","SOL","XRP","ADA","DOGE","AVAX"];

const PLANS = [
  { id:"bronze",   name:"Bronze",   clr:"#CD7F32", glow:"rgba(205,127,50,0.15)",  icon:"🥉", min:200,    max:4999,   daily:3.0, referral:10, features:["3% Daily Returns","10% Referral Bonus","Compounding Interest","24/7 Support","Basic Analytics"] },
  { id:"silver",   name:"Silver",   clr:"#C0C0C0", glow:"rgba(192,192,192,0.12)", icon:"🥈", min:5000,   max:19999,  daily:5.5, referral:10, features:["5.5% Daily Returns","10% Referral Bonus","Compounding Interest","Priority Support","Advanced Analytics"] },
  { id:"gold",     name:"Gold",     clr:"#FFD700", glow:"rgba(255,215,0,0.15)",   icon:"🥇", min:20000,  max:49999,  daily:8.0, referral:10, features:["8% Daily Returns","10% Referral Bonus","Compounding Interest","VIP Support","Full Analytics Suite"] },
  { id:"platinum", name:"Platinum", clr:"#E5E4E2", glow:"rgba(229,228,226,0.12)", icon:"💎", min:50000,  max:null,   daily:12.0,referral:10, features:["12% Daily Returns","10% Referral Bonus","Compounding Interest","Dedicated Manager","Institutional Analytics"] },
];

const SEED = {
  BTC:  {usd: 76489.00, ch:  0.21},
  ETH:  {usd:  2110.15, ch: -0.87},
  USDT: {usd:     1.00, ch:  0.00},
  BNB:  {usd:   675.36, ch:  0.16},
  SOL:  {usd:    89.34, ch: -1.55},
  XRP:  {usd:    1.440, ch: -0.08},
  ADA:  {usd:   0.6800, ch: -0.50},
  DOGE: {usd:   0.1050, ch: -1.71},
  AVAX: {usd:    9.140, ch:  0.16},
};

/* ─────────────────────────────────────────────
   REAL-TIME PRICE HOOK
   Uses Anthropic API with web_search tool to
   fetch current prices from the web every 60s.
   Falls back to animated seed prices instantly.
───────────────────────────────────────────── */
function usePrices() {
  const [prices, setPrices] = useState(SEED);
  const [lastUpdate, setLastUpdate] = useState(null);
  const [fetching, setFetching] = useState(false);

  // Smooth micro-drift so numbers always visually tick between real fetches
  useEffect(() => {
    const id = setInterval(() => {
      setPrices(prev => {
        const next = {};
        for (const [sym, val] of Object.entries(prev)) {
          if (sym === "USDT") { next[sym] = val; continue; }
          const drift = 1 + (Math.random() - 0.499) * 0.0006;
          next[sym] = {
            usd: parseFloat((val.usd * drift).toFixed(
              ["XRP","ADA","DOGE"].includes(sym) ? 4 : 2
            )),
            ch: parseFloat((val.ch + (Math.random() - 0.5) * 0.015).toFixed(2)),
          };
        }
        return next;
      });
    }, 3000);
    return () => clearInterval(id);
  }, []);

  // Fetch real prices from CoinMarketCap via Anthropic web_search
  const fetchPrices = useCallback(async () => {
    if (fetching) return;
    setFetching(true);
    try {
      const resp = await fetch("https://api.anthropic.com/v1/messages", {
        method: "POST",
        headers: {
          "content-type": "application/json",
          "anthropic-version": "2023-06-01",
        },
        body: JSON.stringify({
          model: "claude-sonnet-4-20250514",
          max_tokens: 1024,
          tools: [{ type: "web_search_20250305", name: "web_search" }],
          system: "You are a crypto price bot. Search for live prices and respond with ONLY a raw JSON object. No markdown, no explanation, no extra text whatsoever.",
          messages: [{
            role: "user",
            content: `Search coinmarketcap.com right now for the exact current USD prices of BTC, ETH, USDT, BNB, SOL, XRP, ADA, DOGE, AVAX. Return ONLY this exact JSON with real values filled in (no markdown fences, no text before or after):
{"BTC":{"usd":0,"ch":0},"ETH":{"usd":0,"ch":0},"USDT":{"usd":1,"ch":0},"BNB":{"usd":0,"ch":0},"SOL":{"usd":0,"ch":0},"XRP":{"usd":0,"ch":0},"ADA":{"usd":0,"ch":0},"DOGE":{"usd":0,"ch":0},"AVAX":{"usd":0,"ch":0}}`,
          }],
        }),
      });

      if (!resp.ok) throw new Error(`HTTP ${resp.status}`);
      const body = await resp.json();

      const raw = (body.content || [])
        .filter(b => b.type === "text")
        .map(b => b.text)
        .join("");

      // Extract JSON — look for object containing BTC key
      const match = raw.match(/\{[^{}]*"BTC"[^{}]*\}/s) || raw.match(/\{[\s\S]*?"BTC"[\s\S]*?\}/);
      if (!match) throw new Error("No JSON block found");

      const json = JSON.parse(match[0]);

      const next = { ...prices };
      let updated = 0;
      for (const sym of Object.keys(SEED)) {
        const entry = json[sym];
        if (entry && typeof entry.usd === "number" && entry.usd > 0) {
          next[sym] = { usd: entry.usd, ch: typeof entry.ch === "number" ? entry.ch : 0 };
          updated++;
        }
      }
      if (updated >= 2) {
        setPrices(next);
        setLastUpdate(new Date());
      }
    } catch (e) {
      console.warn("Price fetch failed:", e.message);
    } finally {
      setFetching(false);
    }
  }, [fetching]);

  useEffect(() => {
    // Fire immediately, then every 30 seconds
    fetchPrices();
    const id = setInterval(fetchPrices, 30000);
    return () => clearInterval(id);
  }, []);

  const fmt = (px) => {
    if (px >= 1000) return `$${px.toLocaleString("en-US", {minimumFractionDigits:2, maximumFractionDigits:2})}`;
    if (px >= 1)    return `$${px.toFixed(4)}`;
    return `$${px.toFixed(6)}`;
  };

  const COINS = Object.fromEntries(
    Object.entries(COIN_META).map(([k, m]) => [k, { ...m, px: prices[k].usd, ch: prices[k].ch }])
  );

  const TICKS = TICK_META.map(s => {
    const d = prices[s];
    return { s, p: fmt(d.usd, s), c: `${d.ch >= 0 ? "+" : ""}${d.ch.toFixed(2)}%`, up: d.ch >= 0 };
  });

  return { COINS, TICKS, lastUpdate, fetching, connected: !!lastUpdate, refresh: fetchPrices };
}

/* ── QR ── */
function QR({ val, size = 150 }) {
  const n = 23, cell = size / n;
  const seed = val.split("").reduce((a, c) => a + c.charCodeAt(0), 0);
  const rng = i => { const x = Math.sin(seed + i) * 9999; return x - Math.floor(x); };
  const finder = (r, c) => {
    const ps = [[0,0],[0,n-7],[n-7,0]];
    return ps.some(([pr,pc]) =>
      r>=pr&&r<=pr+6&&c>=pc&&c<=pc+6&&!(r>pr&&r<pr+6&&c>pc&&c<pc+6)
      ||r>=pr+2&&r<=pr+4&&c>=pc+2&&c<=pc+4
    );
  };
  return (
    <svg width={size} height={size} viewBox={`0 0 ${size} ${size}`} style={{display:"block",borderRadius:8,flexShrink:0}}>
      <rect width={size} height={size} fill="#fff"/>
      {Array.from({length:n}).map((_,r) => Array.from({length:n}).map((_,c) => {
        const dark = finder(r,c) || rng(r*n+c) > 0.48;
        return dark ? <rect key={`${r}${c}`} x={c*cell} y={r*cell} width={cell} height={cell} fill="#080B14"/> : null;
      }))}
    </svg>
  );
}

/* ── Scrolling ticker ── */
function TickerScroll({ TICKS }) {
  const [x, setX] = useState(0);
  const ref = useRef(null);
  useEffect(() => {
    let raf, prev = 0;
    const run = t => {
      if (prev) { const sw = ref.current?.scrollWidth || 1600; setX(p => (p - (t-prev)*0.045) % (sw/2)); }
      prev = t; raf = requestAnimationFrame(run);
    };
    raf = requestAnimationFrame(run);
    return () => cancelAnimationFrame(raf);
  }, []);
  const items = [...TICKS, ...TICKS];
  return (
    <div ref={ref} style={{display:"flex", transform:`translateX(${x}px)`, whiteSpace:"nowrap", flex:1}}>
      {items.map((t, i) => (
        <div key={i} style={{display:"inline-flex",alignItems:"center",gap:6,padding:"0 20px",
          borderRight:"1px solid rgba(120,140,200,0.05)"}}>
          <span style={{fontSize:11,fontWeight:700,color:"#546190"}}>{t.s}</span>
          <span style={{fontSize:11,fontWeight:600,color:"#B0B0C8"}}>{t.p}</span>
          <span style={{fontSize:11,fontWeight:800,color:t.up?G:"#FF4757"}}>{t.c}</span>
        </div>
      ))}
    </div>
  );
}

/* ── Chart Tooltip ── */
function Tip({ active, payload, label }) {
  if (!active || !payload?.length) return null;
  return (
    <div style={{background:"rgba(13,13,20,0.97)",border:`1px solid ${G}30`,borderRadius:10,padding:"10px 14px"}}>
      <p style={{margin:"0 0 3px",fontSize:11,color:"#6B7BA4"}}>{label}</p>
      <p style={{margin:0,fontSize:13,fontWeight:700,color:G}}>${payload[0].value.toLocaleString()}</p>
    </div>
  );
}

/* ── Card ── */
const Card = ({ children, style = {} }) => {
  const { T } = useTheme();
  return (
    <div style={{
      background: T.card,
      border: `1px solid ${T.border}`,
      backdropFilter:"blur(18px)",
      WebkitBackdropFilter:"blur(18px)",
      borderRadius:12,
      ...style
    }}>{children}</div>
  );
};

/* ── Sign In Screen ── */
/* ── Shared form input style ── */
const AUTH_INP = {
  width:"100%", padding:"10px 13px", borderRadius:9,
  background:"rgba(120,140,200,0.07)", border:"1px solid rgba(120,140,200,0.14)",
  color:"#E8EAF6", fontSize:13, outline:"none",
  boxSizing:"border-box", fontFamily:"inherit", transition:"border-color .18s",
};

/* ── Animated Background Canvas ── */

/* ── Animated Background (CSS only — no canvas) ── */
function AnimatedBG() {
  return (
    <div style={{position:"fixed",inset:0,zIndex:0,pointerEvents:"none",overflow:"hidden"}}>
      <div style={{position:"absolute",top:"-20%",left:"-10%",width:"55vw",height:"55vw",borderRadius:"50%",
        background:"radial-gradient(circle,rgba(201,168,76,0.09) 0%,transparent 65%)",
        animation:"float 9s ease-in-out infinite"}}/>
      <div style={{position:"absolute",bottom:"-20%",right:"-10%",width:"60vw",height:"60vw",borderRadius:"50%",
        background:"radial-gradient(circle,rgba(124,111,205,0.08) 0%,transparent 65%)",
        animation:"float 11s ease-in-out infinite reverse"}}/>
      <div style={{position:"absolute",top:"35%",left:"30%",width:"40vw",height:"40vw",borderRadius:"50%",
        background:"radial-gradient(circle,rgba(79,195,247,0.05) 0%,transparent 60%)",
        animation:"pulse-glow 7s ease-in-out infinite"}}/>
    </div>
  );
}

/* ── Portfolio Ring (CSS + SVG, no RAF canvas) ── */

/* ── Portfolio Ring — Canvas animated with glow ── */
function DashboardRing({ txns, now, go }) {
  const { T } = useTheme();
  const canvasRef = useRef(null);
  const rafRef    = useRef(null);
  const rotRef    = useRef(0);
  const pulseRef  = useRef(0);

  const totalDeposited = txns.reduce((s,t)=>s+t.usdValue,0);
  const totalProfit    = txns.reduce((s,t)=>{
    const secs=(now-t.timestamp)/1000;
    return s+t.usdValue*(t.planDaily/100)*(secs/86400);
  },0);
  const totalValue = totalDeposited+totalProfit;
  const activePlan = txns.length ? PLANS.find(p=>p.id===txns[0].planId) : null;
  const planIdx    = activePlan ? PLANS.findIndex(p=>p.id===activePlan.id) : -1;
  const nextPlan   = planIdx>=0 ? PLANS[Math.min(planIdx+1,PLANS.length-1)] : PLANS[0];
  const planMin    = activePlan?.min??0;
  const planMax    = activePlan?.max??nextPlan.min;
  const progress   = planMax&&totalValue>planMin
    ? Math.min((totalValue-planMin)/(planMax-planMin),1):0;

  useEffect(()=>{
    const canvas = canvasRef.current;
    if(!canvas) return;
    let mounted = true;
    const dpr = Math.min(window.devicePixelRatio||1, 2);
    const SIZE = 240;
    canvas.width  = SIZE*dpr;
    canvas.height = SIZE*dpr;
    canvas.style.width  = SIZE+"px";
    canvas.style.height = SIZE+"px";
    const ctx = canvas.getContext("2d");
    ctx.scale(dpr, dpr);

    const CX=120, CY=120, R=88, SW=15;
    const RED_DEG  = 300; // degrees for red arc
    const BLUE_DEG = 55;  // degrees for blue arc
    const toRad = d => d*(Math.PI/180);

    // Particle dots on the ring
    const dots = Array.from({length:8},(_,i)=>({
      angle: (i/8)*Math.PI*2,
      speed: 0.006+Math.random()*0.004,
      r:     R+10+Math.random()*16,
      size:  Math.random()*1.4+0.4,
      alpha: Math.random()*0.5+0.2,
      clr:   Math.random()>0.5 ? [255,77,109] : [201,168,76],
    }));

    const draw = ()=>{
      if(!mounted) return;
      rotRef.current  += 0.008;   // slow ring rotation
      pulseRef.current+= 0.05;    // glow pulse
      const rot   = rotRef.current;
      const pulse = 0.5+0.5*Math.sin(pulseRef.current);

      ctx.clearRect(0,0,SIZE,SIZE);

      // ── 1. Outer glow halo ──
      const halo = ctx.createRadialGradient(CX,CY,R-10,CX,CY,R+18);
      halo.addColorStop(0,`rgba(255,77,109,${0.06+pulse*0.04})`);
      halo.addColorStop(1,"rgba(255,77,109,0)");
      ctx.beginPath(); ctx.arc(CX,CY,R+18,0,Math.PI*2);
      ctx.fillStyle=halo; ctx.fill();

      // ── 2. Track ──
      ctx.beginPath(); ctx.arc(CX,CY,R,0,Math.PI*2);
      ctx.strokeStyle="rgba(255,255,255,0.05)";
      ctx.lineWidth=SW; ctx.stroke();

      // ── 3. RED arc — 300° rotating ──
      const redStart = -Math.PI/2 + rot*0.12;
      const redEnd   = redStart + toRad(RED_DEG);

      // glow shadow
      ctx.save();
      ctx.shadowColor=`rgba(255,55,100,${0.45+pulse*0.25})`;
      ctx.shadowBlur=18;
      ctx.beginPath(); ctx.arc(CX,CY,R,redStart,redEnd);
      const redG = ctx.createLinearGradient(
        CX+R*Math.cos(redStart),CY+R*Math.sin(redStart),
        CX+R*Math.cos(redEnd),  CY+R*Math.sin(redEnd)
      );
      redG.addColorStop(0,"#FF6B8A");
      redG.addColorStop(0.5,"#FF2255");
      redG.addColorStop(1,"#C9184A");
      ctx.strokeStyle=redG;
      ctx.lineWidth=SW; ctx.lineCap="round"; ctx.stroke();
      ctx.restore();

      // bright leading dot on red tip
      const rdx=CX+R*Math.cos(redEnd), rdy=CY+R*Math.sin(redEnd);
      const rdg=ctx.createRadialGradient(rdx,rdy,0,rdx,rdy,10);
      rdg.addColorStop(0,"rgba(255,200,210,0.9)");
      rdg.addColorStop(0.4,"rgba(255,100,130,0.5)");
      rdg.addColorStop(1,"rgba(255,77,109,0)");
      ctx.beginPath(); ctx.arc(rdx,rdy,10,0,Math.PI*2);
      ctx.fillStyle=rdg; ctx.fill();

      // ── 4. BLUE arc — 55°, offset + slow counter-rotate ──
      const blueOffset = Math.PI*0.85 - rot*0.05;
      const blueEnd    = blueOffset + toRad(BLUE_DEG);

      ctx.save();
      ctx.shadowColor=`rgba(79,195,247,${0.4+pulse*0.2})`;
      ctx.shadowBlur=20;
      ctx.beginPath(); ctx.arc(CX,CY,R-1,blueOffset,blueEnd);
      const blueG=ctx.createLinearGradient(
        CX+(R-1)*Math.cos(blueOffset),CY+(R-1)*Math.sin(blueOffset),
        CX+(R-1)*Math.cos(blueEnd),   CY+(R-1)*Math.sin(blueEnd)
      );
      blueG.addColorStop(0,"#7C6FCD");
      blueG.addColorStop(1,"#4FC3F7");
      ctx.strokeStyle=blueG;
      ctx.lineWidth=SW-4; ctx.lineCap="round"; ctx.stroke();
      ctx.restore();

      // blue leading dot
      const bdx=CX+(R-1)*Math.cos(blueEnd), bdy=CY+(R-1)*Math.sin(blueEnd);
      const bdg=ctx.createRadialGradient(bdx,bdy,0,bdx,bdy,9);
      bdg.addColorStop(0,"rgba(180,220,255,0.9)");
      bdg.addColorStop(0.5,"rgba(79,195,247,0.5)");
      bdg.addColorStop(1,"rgba(79,195,247,0)");
      ctx.beginPath(); ctx.arc(bdx,bdy,9,0,Math.PI*2);
      ctx.fillStyle=bdg; ctx.fill();

      // ── 5. Orbiting particles ──
      dots.forEach(p=>{
        p.angle += p.speed;
        const px=CX+p.r*Math.cos(p.angle);
        const py=CY+p.r*Math.sin(p.angle);
        const a = p.alpha*(0.6+0.4*Math.sin(p.angle*4));
        ctx.beginPath(); ctx.arc(px,py,p.size,0,Math.PI*2);
        ctx.fillStyle=`rgba(${p.clr[0]},${p.clr[1]},${p.clr[2]},${a})`;
        ctx.fill();
      });

      // ── 6. Inner dark fill ──
      const inner=ctx.createRadialGradient(CX,CY-10,0,CX,CY,R-SW/2-3);
      inner.addColorStop(0,"rgba(22,10,44,0.98)");
      inner.addColorStop(1,"rgba(8,8,20,0.97)");
      ctx.beginPath(); ctx.arc(CX,CY,R-SW/2-3,0,Math.PI*2);
      ctx.fillStyle=inner; ctx.fill();

      // inner glow
      const ig=ctx.createRadialGradient(CX,CY,0,CX,CY,55);
      ig.addColorStop(0,`rgba(201,168,76,${0.04+pulse*0.03})`);
      ig.addColorStop(1,"rgba(201,168,76,0)");
      ctx.beginPath(); ctx.arc(CX,CY,55,0,Math.PI*2);
      ctx.fillStyle=ig; ctx.fill();

      rafRef.current=requestAnimationFrame(draw);
    };

    rafRef.current=requestAnimationFrame(draw);
    return ()=>{ mounted=false; cancelAnimationFrame(rafRef.current); };
  },[]);

  return (
    <div style={{borderRadius:18,padding:"20px 16px 18px",
      background:"linear-gradient(160deg,rgba(18,6,38,0.96),rgba(8,11,26,0.98))",
      border:"1px solid rgba(201,168,76,0.22)",backdropFilter:"blur(22px)",
      position:"relative",overflow:"hidden"}}>

      <div style={{position:"absolute",top:0,left:0,right:0,height:1,
        background:"linear-gradient(90deg,transparent,rgba(201,168,76,0.8),rgba(255,77,109,0.4),transparent)",
        backgroundSize:"200% 100%",animation:"shimmer 2.5s linear infinite"}}/>
      <div style={{position:"absolute",top:-50,left:"50%",transform:"translateX(-50%)",
        width:240,height:160,borderRadius:"50%",pointerEvents:"none",
        background:"radial-gradient(ellipse,rgba(201,168,76,0.07),transparent 70%)"}}/>

      <div style={{textAlign:"center",marginBottom:6}}>
        <span style={{fontSize:9,fontWeight:700,color:G,letterSpacing:2.2,textTransform:"uppercase"}}>
          ◈ Portfolio Ring
        </span>
      </div>

      {/* Canvas ring */}
      <div style={{display:"flex",justifyContent:"center",position:"relative"}}>
        <canvas ref={canvasRef} style={{display:"block"}}/>

        {/* Center overlay */}
        <div style={{position:"absolute",top:"50%",left:"50%",
          transform:"translate(-50%,-50%)",
          textAlign:"center",width:152,pointerEvents:"none"}}>
          <div style={{
            fontSize:totalValue>=100000?15:totalValue>=10000?17:totalValue>=1000?20:23,
            fontWeight:900,letterSpacing:"-1.2px",lineHeight:1,marginBottom:5,
            background:`linear-gradient(135deg,${G2},${G})`,
            WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent",
          }}>
            {totalValue>0
              ?`$${totalValue.toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}`
              :"$0.00"}
          </div>
          <div style={{fontSize:8,color:T.textSub,letterSpacing:1.2,
            textTransform:"uppercase",fontWeight:600,marginBottom:9}}>Total Value</div>
          {activePlan
            ?<div style={{display:"inline-block",padding:"4px 11px",borderRadius:999,
                background:`${activePlan.clr}18`,border:`1px solid ${activePlan.clr}35`,
                fontSize:10,fontWeight:700,color:activePlan.clr,
                boxShadow:`0 0 10px ${activePlan.clr}20`}}>
                {activePlan.icon} {activePlan.name}
              </div>
            :<button onClick={()=>go("plans")} style={{fontSize:9,color:G,
                background:`${G}10`,border:`1px solid ${G}28`,
                cursor:"pointer",fontWeight:700,padding:"4px 10px",borderRadius:999}}>
                Start Investing →
              </button>
          }
        </div>
      </div>

      {/* 3 stat cards */}
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:9,marginTop:-6}}>
        {[
          {label:"Deposited",  val:`$${totalDeposited.toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}`,clr:T.text},
          {label:"Live Profit",val:`+$${totalProfit.toFixed(4)}`,clr:G},
          {label:"Next Tier",  val:activePlan?.id==="platinum"?"MAX":`$${nextPlan.min.toLocaleString()}`,clr:nextPlan.clr},
        ].map(({label,val,clr})=>(
          <div key={label} style={{textAlign:"center",padding:"10px 5px",borderRadius:10,
            background:"rgba(120,140,200,0.04)",border:"1px solid rgba(120,140,200,0.09)"}}>
            <div style={{fontSize:8,color:T.textSub,marginBottom:4,textTransform:"uppercase",
              letterSpacing:.7,fontWeight:700}}>{label}</div>
            <div style={{fontSize:11,fontWeight:800,color:clr,
              fontVariantNumeric:"tabular-nums"}}>{val}</div>
          </div>
        ))}
      </div>

      {/* Progress bar */}
      {activePlan&&activePlan.id!=="platinum"&&(
        <div style={{marginTop:12}}>
          <div style={{display:"flex",justifyContent:"space-between",marginBottom:5}}>
            <span style={{fontSize:9,color:T.textSub}}>Progress to {nextPlan.name}</span>
            <span style={{fontSize:9,color:G,fontWeight:700}}>{(progress*100).toFixed(1)}%</span>
          </div>
          <div style={{height:5,borderRadius:999,
            background:"rgba(255,255,255,0.05)",overflow:"hidden",
            boxShadow:"inset 0 1px 3px rgba(0,0,0,0.3)"}}>
            <div style={{height:"100%",borderRadius:999,
              background:"linear-gradient(90deg,#FF4D6D,#C9A84C,#E8C97A)",
              width:`${Math.max(progress*100,2)}%`,
              transition:"width 1.4s cubic-bezier(0.4,0,0.2,1)",
              boxShadow:"0 0 10px rgba(201,168,76,0.55)"}}/>
          </div>
        </div>
      )}
    </div>
  );
}

/* ── Distribution Banner (CSS only, no RAF) ── */
function DistributionBanner({ txns, now }) {
  const { T } = useTheme();
  const PLATFORM_BASE = 2847693.45;
  const PLATFORM_PCT  = 165.3;
  const [display, setDisplay] = useState(0);
  const [pct,     setPct]     = useState(0);

  const totalProfit = txns.reduce((s,t)=>{
    const secs=(now-t.timestamp)/1000;
    return s+t.usdValue*(t.planDaily/100)*(secs/86400);
  },0);
  const liveTotal = PLATFORM_BASE + totalProfit;

  useEffect(()=>{
    let f=0; const tot=70;
    const easeOut = t => 1-Math.pow(2,-10*t);
    const id = setInterval(()=>{
      f++; const e=easeOut(Math.min(f/tot,1));
      setDisplay(liveTotal*e); setPct(PLATFORM_PCT*e);
      if(f>=tot){ setDisplay(liveTotal); setPct(PLATFORM_PCT); clearInterval(id); }
    },20);
    return()=>clearInterval(id);
  },[]);

  useEffect(()=>setDisplay(liveTotal),[liveTotal]);

  return (
    <div style={{borderRadius:16,padding:"16px",
      background:"linear-gradient(145deg,rgba(14,8,36,0.95),rgba(8,16,36,0.95))",
      border:"1px solid rgba(124,111,205,0.25)",backdropFilter:"blur(20px)",
      position:"relative",overflow:"hidden"}}>
      <div style={{position:"absolute",top:0,left:0,right:0,height:1,
        background:"linear-gradient(90deg,transparent,rgba(124,111,205,0.8),rgba(79,195,247,0.5),transparent)",
        backgroundSize:"200% 100%",animation:"shimmer 2s linear infinite"}}/>
      <div style={{position:"absolute",bottom:-30,right:-30,width:110,height:110,borderRadius:"50%",
        background:"radial-gradient(circle,rgba(79,195,247,0.10),transparent 70%)",pointerEvents:"none"}}/>
      <div style={{display:"flex",alignItems:"center",gap:7,marginBottom:12}}>
        <div style={{width:6,height:6,borderRadius:"50%",background:ACCENT2,
          boxShadow:`0 0 8px ${ACCENT2}`,animation:"blink 1.5s infinite"}}/>
        <span style={{fontSize:9,fontWeight:700,color:ACCENT2,letterSpacing:1.8,textTransform:"uppercase"}}>
          Total Platform Distribution
        </span>
        <div style={{marginLeft:"auto",display:"flex",alignItems:"center",gap:4,
          padding:"2px 7px",borderRadius:999,
          background:"rgba(74,222,128,0.08)",border:"1px solid rgba(74,222,128,0.2)"}}>
          <div style={{width:4,height:4,borderRadius:"50%",background:"#4ADE80",animation:"blink 1s infinite"}}/>
          <span style={{fontSize:8,color:"#4ADE80",fontWeight:700}}>LIVE</span>
        </div>
      </div>
      <div style={{textAlign:"center",marginBottom:12}}>
        <div style={{fontSize:30,fontWeight:900,letterSpacing:"-1.5px",lineHeight:1,
          background:`linear-gradient(135deg,#FFFFFF,${ACCENT3},${ACCENT2})`,
          WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent",
          marginBottom:4,fontVariantNumeric:"tabular-nums"}}>
          ${display.toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}
        </div>
        <div style={{fontSize:10,color:T.textSub,marginBottom:8}}>USDT distributed to investors worldwide</div>
        <div style={{display:"inline-flex",alignItems:"center",gap:6,
          padding:"5px 14px",borderRadius:999,
          background:"rgba(79,195,247,0.08)",border:"1px solid rgba(79,195,247,0.20)"}}>
          <TrendingUp size={11} color={ACCENT3} strokeWidth={2.5}/>
          <span style={{fontSize:11,fontWeight:800,color:"#E8EAF6"}}>
            Over <span style={{color:ACCENT3}}>{pct.toFixed(1)}%</span> returns paid out
          </span>
        </div>
      </div>
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:7,marginBottom:12}}>
        {[
          {label:"Active Investors",val:"2,847",   clr:ACCENT2,icon:"👥"},
          {label:"Avg Daily Return", val:"6.6%",   clr:G,      icon:"📈"},
          {label:"Since Launch",     val:"May 2024",clr:ACCENT3,icon:"🚀"},
        ].map(({label,val,clr,icon})=>(
          <div key={label} style={{textAlign:"center",padding:"9px 5px",borderRadius:9,
            background:"rgba(124,111,205,0.06)",border:"1px solid rgba(124,111,205,0.13)"}}>
            <div style={{fontSize:12,marginBottom:2}}>{icon}</div>
            <div style={{fontSize:11,fontWeight:800,color:clr,marginBottom:1}}>{val}</div>
            <div style={{fontSize:8,color:T.textMuted,letterSpacing:.3}}>{label}</div>
          </div>
        ))}
      </div>
      <div>
        <div style={{display:"flex",justifyContent:"space-between",marginBottom:5}}>
          <span style={{fontSize:9,color:T.textSub}}>🏆 Next milestone: $5M</span>
          <span style={{fontSize:9,color:ACCENT2,fontWeight:800}}>{Math.min((display/5000000)*100,100).toFixed(1)}%</span>
        </div>
        <div style={{height:5,borderRadius:999,background:"rgba(124,111,205,0.10)",overflow:"hidden"}}>
          <div style={{height:"100%",borderRadius:999,
            background:`linear-gradient(90deg,${ACCENT2},${ACCENT3})`,
            width:`${Math.min((display/5000000)*100,100)}%`,
            boxShadow:`0 0 10px ${ACCENT2}70`,transition:"width 2.5s ease"}}/>
        </div>
      </div>
      {totalProfit>0&&(
        <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",
          marginTop:10,padding:"8px 11px",borderRadius:9,
          background:`${G}08`,border:`1px solid ${G}18`}}>
          <span style={{fontSize:10,color:T.textSub}}>Your contribution</span>
          <span style={{fontSize:11,fontWeight:800,color:G,fontVariantNumeric:"tabular-nums"}}>
            +${totalProfit.toFixed(4)} USDT
          </span>
        </div>
      )}
    </div>
  );
}

function Sidebar({ active, go, open, onClose }) {
  const { T } = useTheme();
  const nav = [
    {id:"dashboard",   Icon:LayoutDashboard, label:"Dashboard"},
    {id:"plans",       Icon:Star,            label:"Plans"},
    {id:"deposit",     Icon:ArrowDownToLine, label:"Deposit"},
    {id:"withdraw",    Icon:ArrowUpFromLine, label:"Withdraw"},
    {id:"transactions",Icon:List,            label:"Transactions"},
  ];
  return (
    <>
      {open && <div onClick={onClose} style={{position:"fixed",inset:0,background:"rgba(0,0,0,0.7)",zIndex:40,backdropFilter:"blur(2px)"}}/>}
      <aside style={{
        width:190,flexShrink:0,display:"flex",flexDirection:"column",
        background:T.sidebar,
        borderRight:`1px solid ${T.border}`,
        backdropFilter:"blur(24px)",
        WebkitBackdropFilter:"blur(24px)",
        height:"100%",zIndex:50,
        position:"fixed",top:0,left:0,bottom:0,
        transition:"transform 0.3s ease, background 0.35s ease",
        transform: open ? "translateX(0)" : "translateX(-100%)",
      }}>
        <button onClick={onClose} style={{position:"absolute",top:12,right:12,width:28,height:28,
          borderRadius:8,background:"rgba(120,140,200,0.10)",border:"none",cursor:"pointer",
          color:"#6B7BA4",display:"flex",alignItems:"center",justifyContent:"center"}}>
          <X size={14}/>
        </button>
        <div style={{padding:"18px 18px 16px",borderBottom:"1px solid rgba(201,168,76,0.12)"}}>
          <div style={{display:"flex",alignItems:"center",gap:11}}>
            {/* AetherLink Logo Mark */}
            <div style={{width:38,height:38,flexShrink:0,position:"relative"}}>
              <svg width="38" height="38" viewBox="0 0 38 38" fill="none" xmlns="http://www.w3.org/2000/svg">
                <defs>
                  <linearGradient id="lgSide" x1="0" y1="0" x2="38" y2="38" gradientUnits="userSpaceOnUse">
                    <stop offset="0%" stopColor="#E8C97A"/>
                    <stop offset="50%" stopColor="#C9A84C"/>
                    <stop offset="100%" stopColor="#A07830"/>
                  </linearGradient>
                  <linearGradient id="lgSide2" x1="0" y1="0" x2="38" y2="38" gradientUnits="userSpaceOnUse">
                    <stop offset="0%" stopColor="#7C6FCD"/>
                    <stop offset="100%" stopColor="#4FC3F7"/>
                  </linearGradient>
                  <filter id="glow">
                    <feGaussianBlur stdDeviation="1.5" result="blur"/>
                    <feMerge><feMergeNode in="blur"/><feMergeNode in="SourceGraphic"/></feMerge>
                  </filter>
                </defs>
                {/* Hexagon background */}
                <path d="M19 2 L34 10.5 L34 27.5 L19 36 L4 27.5 L4 10.5 Z"
                  fill="rgba(201,168,76,0.08)" stroke="url(#lgSide)" strokeWidth="1"/>
                {/* Inner diamond */}
                <path d="M19 8 L28 19 L19 30 L10 19 Z"
                  fill="none" stroke="url(#lgSide2)" strokeWidth="0.8" opacity="0.6"/>
                {/* A letterform - stylized */}
                <path d="M19 9 L27 28 H23.5 L21.8 23.5 H16.2 L14.5 28 H11 Z M17.2 20.5 H20.8 L19 15.5 Z"
                  fill="url(#lgSide)" filter="url(#glow)"/>
                {/* accent dot */}
                <circle cx="19" cy="5" r="1.5" fill="#E8C97A" opacity="0.9"/>
              </svg>
            </div>
            <div>
              <div style={{fontSize:12,fontWeight:700,color:"#E8EAF6",lineHeight:1.2,letterSpacing:"-.2px"}}>AetherLink</div>
              <div style={{fontSize:9,color:"#C9A84C",letterSpacing:1.8,textTransform:"uppercase",marginTop:1,fontWeight:600}}>Capital</div>
            </div>
          </div>
        </div>
        <nav style={{flex:1,padding:"10px 8px",overflowY:"auto"}}>
          <div style={{fontSize:9,color:"#3D4F7C",letterSpacing:1.5,textTransform:"uppercase",padding:"8px 10px 6px",fontWeight:700}}>Menu</div>
          {nav.map(({id,Icon,label}) => {
            const on = active === id;
            return (
              <button key={id} onClick={() => { go(id); onClose(); }} style={{
                width:"100%",display:"flex",alignItems:"center",gap:10,
                padding:"10px 12px",borderRadius:10,border:"none",cursor:"pointer",marginBottom:2,
                background:on?`${G}14`:"transparent",color:on?G:T.textSub,
                fontWeight:on?700:500,fontSize:13,textAlign:"left",transition:"all .15s",outline:"none",
                boxShadow:on?`inset 0 0 0 1px ${G}35,0 0 12px ${G}15`:"none",
              }}>
                <Icon size={16} strokeWidth={on?2.5:1.8} style={{flexShrink:0}}/>
                {label}
              </button>
            );
          })}
        </nav>
      </aside>
    </>
  );
}

/* ── Topbar ── */
function Topbar({ screen, onMenu, COINS, lastUpdate, fetching, connected, refresh, dark, toggleTheme }) {
  const { T } = useTheme();
  const TITLE = {dashboard:"Dashboard",plans:"Investment Plans",deposit:"Deposit",withdraw:"Withdraw",
    transactions:"Transactions"};
  const [now, setNow] = useState("");
  useEffect(() => {
    const f = () => setNow(new Date().toLocaleTimeString("en-US",{hour:"2-digit",minute:"2-digit"}));
    f(); const id = setInterval(f, 15000); return () => clearInterval(id);
  }, []);

  const chips = [
    {sym:"BTC",clr:"#F7931A",icon:"₿"},
    {sym:"ETH",clr:"#627EEA",icon:"Ξ"},
    {sym:"USDT",clr:"#26A17B",icon:"₮"},
  ].map(c => ({...c, coin: COINS[c.sym]}));

  return (
    <header style={{height:"auto",minHeight:54,display:"flex",alignItems:"center",justifyContent:"space-between",
      padding:"6px 14px",borderBottom:"1px solid rgba(120,140,200,0.10)",
      background:T.header,backdropFilter:"blur(24px)",borderBottom:`1px solid ${T.border}`,
      position:"sticky",top:0,zIndex:30,flexShrink:0,width:"100%",boxSizing:"border-box",gap:8}}>

      {/* left */}
      <div style={{display:"flex",alignItems:"center",gap:10,flexShrink:0}}>
        <button onClick={onMenu} style={{width:30,height:30,borderRadius:9,
          background:"rgba(120,140,200,0.07)",border:"1px solid rgba(120,140,200,0.13)",
          display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",color:"#6B7BA4"}}>
          <Menu size={16}/>
        </button>
        <div>
          <h1 style={{margin:0,fontSize:14,fontWeight:700,color:"#E8EAF6",letterSpacing:"-.4px",lineHeight:1}}>{TITLE[screen]}</h1>
          <p style={{margin:"2px 0 0",fontSize:10,color:"#3D4F7C"}}>
            {new Date().toLocaleDateString("en-US",{month:"short",day:"numeric",year:"numeric"})} · {now}
          </p>
        </div>
      </div>

      {/* center — price chips, stacked compactly */}
      <div style={{display:"flex",flexDirection:"column",gap:4,flex:1,alignItems:"center"}}>
        {chips.map(({sym,clr,icon,coin}) => {
          const px = coin?.px ?? 0;
          const ch = coin?.ch ?? 0;
          const up = ch >= 0;
          const fmtPx = px >= 1000
            ? `$${px.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`
            : `$${px.toFixed(4)}`;
          return (
            <div key={sym} style={{display:"flex",alignItems:"center",gap:5,
              padding:"3px 8px",borderRadius:7,
              background:"rgba(120,140,200,0.05)",
              border:"1px solid rgba(120,140,200,0.12)",
              minWidth:180,justifyContent:"space-between"}}>
              <div style={{display:"flex",alignItems:"center",gap:4}}>
                <span style={{fontSize:10,color:clr,fontWeight:800}}>{icon}</span>
                <span style={{fontSize:10,fontWeight:700,color:"#6A7EAC"}}>{sym}</span>
              </div>
              <span style={{fontSize:11,fontWeight:700,color:"#E8EAF6",
                fontVariantNumeric:"tabular-nums"}}>{fmtPx}</span>
              <span style={{fontSize:10,fontWeight:700,
                color:up?G:"#FF4757",
                background:up?"rgba(0,232,122,0.10)":"rgba(255,71,87,0.10)",
                padding:"1px 5px",borderRadius:4,minWidth:52,textAlign:"center"}}>
                {`${up?"+":""}${ch.toFixed(2)}%`}
              </span>
            </div>
          );
        })}
      </div>

      {/* right */}
      <div style={{display:"flex",alignItems:"center",gap:8,flexShrink:0}}>
        {/* Theme toggle */}
        <button onClick={toggleTheme} title={dark?"Switch to Light Mode":"Switch to Dark Mode"} style={{
          position:"relative",width:56,height:28,borderRadius:14,
          background: dark
            ? "linear-gradient(135deg,#1C1C3A,#2A2A50)"
            : "linear-gradient(135deg,#FFF3CC,#FFE080)",
          border: dark ? "1px solid rgba(201,168,76,0.30)" : "1px solid rgba(201,168,76,0.40)",
          cursor:"pointer",flexShrink:0,
          boxShadow: dark ? "inset 0 1px 3px rgba(0,0,0,0.4)" : "inset 0 1px 3px rgba(0,0,0,0.1)",
          transition:"all 0.35s ease",
          display:"flex",alignItems:"center",
          padding:"0 4px",
        }}>
          {/* Track icons */}
          <Moon size={10} color={dark?"#C9A84C":"#C8C8E8"} style={{
            position:"absolute",left:6,opacity:dark?1:0.3,transition:"opacity 0.3s"}}/>
          <Sun size={10} color={dark?"#4A4A80":"#F59E0B"} style={{
            position:"absolute",right:6,opacity:dark?0.3:1,transition:"opacity 0.3s"}}/>
          {/* Sliding knob */}
          <div style={{
            width:20,height:20,borderRadius:"50%",
            background: dark
              ? "linear-gradient(135deg,#C9A84C,#E8C97A)"
              : "linear-gradient(135deg,#FFFFFF,#FFF8E0)",
            boxShadow: dark
              ? `0 2px 6px rgba(0,0,0,0.5), 0 0 8px ${G}60`
              : "0 2px 6px rgba(0,0,0,0.2)",
            position:"absolute",
            left: dark ? 4 : "calc(100% - 24px)",
            transition:"left 0.35s cubic-bezier(0.4,0,0.2,1)",
            display:"flex",alignItems:"center",justifyContent:"center",
          }}>
            {dark
              ? <Moon size={10} color="#000" style={{opacity:0.8}}/>
              : <Sun size={10} color="#F59E0B"/>
            }
          </div>
        </button>

        <button style={{position:"relative",width:30,height:30,borderRadius:9,
          background:T.borderSub,border:`1px solid ${T.borderSub}`,
          display:"flex",alignItems:"center",justifyContent:"center",cursor:"pointer",color:T.textSub}}>
          <Bell size={15} strokeWidth={1.8}/>
          <span style={{position:"absolute",top:8,right:8,width:6,height:6,borderRadius:"50%",
            background:G,border:`1.5px solid ${T.bg}`,boxShadow:`0 0 5px ${G}`}}/>
        </button>
        <div style={{width:30,height:30,borderRadius:9,
          background:`${G}14`,border:`1px solid ${G}25`,
          display:"flex",alignItems:"center",justifyContent:"center",
          cursor:"pointer"}}>
          <User size={15} color={G}/>
        </div>
      </div>
    </header>
  );
}


/* ── Portfolio Ring Component (Dashboard) ── */

/* ══════════════════════════════════════════════════
   PORTFOLIO RING  —  Canvas-based premium animation
══════════════════════════════════════════════════ */
/* ═══ DASHBOARD ═══ */
function Dashboard({ go, COINS, txns }) {
  const [hide, setHide] = useState(false);
  const [tab,  setTab]  = useState("portfolio");
  const [now,  setNow]  = useState(Date.now());

  // tick every second so profit updates live on dashboard too
  useEffect(() => {
    const id = setInterval(() => setNow(Date.now()), 1000);
    return () => clearInterval(id);
  }, []);

  const lineClr = tab === "btc" ? "#F7931A" : tab === "eth" ? "#627EEA" : G;

  const totalDeposited = txns.reduce((s, t) => s + t.usdValue, 0);
  const totalProfit = txns.reduce((s, t) => {
    const secs = (now - t.timestamp) / 1000;
    return s + t.usdValue * (t.planDaily / 100) * (secs / 86400);
  }, 0);
  const portfolioVal = totalDeposited + totalProfit;

  return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:14,boxSizing:"border-box"}}>

      {/* ── Hero banner ── */}
      <div style={{
        borderRadius:16,padding:"20px 20px 18px",
        background:"linear-gradient(135deg,rgba(201,168,76,0.10) 0%,rgba(124,111,205,0.06) 60%,rgba(8,11,26,0) 100%)",
        border:"1px solid rgba(201,168,76,0.22)",
        position:"relative",overflow:"hidden",
      }}>
        {/* shimmer line */}
        <div style={{position:"absolute",top:0,left:0,right:0,height:1,
          background:"linear-gradient(90deg,transparent,rgba(201,168,76,0.6),transparent)",
          backgroundSize:"200% 100%",animation:"shimmer 3s linear infinite"}}/>
        {/* glow orb */}
        <div style={{position:"absolute",top:-60,right:-40,width:200,height:200,borderRadius:"50%",
          background:`radial-gradient(circle,${G}18,transparent 65%)`,pointerEvents:"none"}}/>

        <div style={{position:"relative",zIndex:1}}>
          <div style={{display:"flex",alignItems:"center",gap:7,marginBottom:6}}>
            <div style={{width:5,height:5,borderRadius:"50%",background:G,
              boxShadow:`0 0 6px ${G}`,animation:"blink 2s infinite"}}/>
            <span style={{fontSize:9,fontWeight:700,color:G,letterSpacing:1.5,textTransform:"uppercase"}}>
              Portfolio Overview
            </span>
          </div>

          <div style={{fontSize:11,color:"#6B7BA4",marginBottom:4,fontWeight:500}}>Total Value</div>
          <div style={{
            fontSize:32,fontWeight:900,letterSpacing:"-1.5px",lineHeight:1,
            background:`linear-gradient(135deg,${G2},${G})`,
            WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent",
            marginBottom:4,
          }}>
            {hide ? "●●●●●●" : `$${portfolioVal.toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}`}
          </div>

          {totalDeposited > 0 && !hide && (
            <div style={{display:"inline-flex",alignItems:"center",gap:5,
              padding:"3px 10px",borderRadius:999,
              background:"rgba(201,168,76,0.10)",border:"1px solid rgba(201,168,76,0.20)",
              marginBottom:14}}>
              <TrendingUp size={10} color={G}/>
              <span style={{fontSize:10,color:G,fontWeight:700}}>
                +${totalProfit.toFixed(4)} live profit
              </span>
            </div>
          )}
          {totalDeposited === 0 && <div style={{marginBottom:14}}/>}

          <div style={{display:"flex",gap:8,flexWrap:"wrap"}}>
            <button onClick={() => setHide(!hide)} style={{
              display:"flex",alignItems:"center",gap:6,padding:"8px 14px",borderRadius:9,
              background:"rgba(120,140,200,0.08)",border:"1px solid rgba(120,140,200,0.15)",
              color:"#7A8DB4",fontSize:12,fontWeight:600,cursor:"pointer",transition:"all .15s"
            }}>
              {hide ? <Eye size={13}/> : <EyeOff size={13}/>} {hide ? "Show" : "Hide"}
            </button>
            <button onClick={() => go("plans")} style={{
              display:"flex",alignItems:"center",gap:6,padding:"8px 14px",borderRadius:9,
              background:"rgba(201,168,76,0.10)",border:"1px solid rgba(201,168,76,0.25)",
              color:G,fontSize:12,fontWeight:700,cursor:"pointer",transition:"all .15s"
            }}>
              <Star size={13}/> Plans
            </button>
            <button onClick={() => go("deposit")} style={{
              display:"flex",alignItems:"center",gap:6,padding:"8px 16px",borderRadius:9,
              background:`linear-gradient(135deg,${G},${GD})`,
              border:"none",color:"#000",fontSize:12,fontWeight:800,cursor:"pointer",
              boxShadow:`0 3px 16px ${G}35`
            }}>
              <ArrowDownToLine size={13}/> Deposit
            </button>
          </div>
        </div>
      </div>

      {/* ── Stat cards ── */}
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}>
        {[
          {label:"Deposited",   val:hide?"●●●":`$${totalDeposited.toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}`, sub:txns.length?`${txns.length} active`:"No deposits", Icon:ArrowDownToLine, clr:"#60A5FA"},
          {label:"Live Profit", val:hide?"●●●":`+$${totalProfit.toFixed(4)}`,                sub:totalDeposited>0?"Counting…":"Start investing", Icon:TrendingUp, clr:G},
          {label:"Active Plans",val:String([...new Set(txns.map(t=>t.planId))].length||0),   sub:txns.length?txns[0].plan+(txns.length>1?` +${txns.length-1}`:""):"No plans", Icon:BarChart3, clr:"#F59E0B"},
          {label:"Assets",      val:"3",                                                       sub:"BTC · ETH · USDT", Icon:Wallet, clr:"#A855F7"},
        ].map(({label,val,sub,Icon,clr}) => (
          <div key={label} style={{
            borderRadius:13,padding:"14px",
            background:"rgba(8,11,26,0.72)",
            border:`1px solid rgba(120,140,200,0.12)`,
            backdropFilter:"blur(18px)",
            position:"relative",overflow:"hidden",
            transition:"border-color .2s",cursor:"default",
          }}
            onMouseEnter={e=>e.currentTarget.style.borderColor=`${clr}30`}
            onMouseLeave={e=>e.currentTarget.style.borderColor="rgba(120,140,200,0.12)"}
          >
            <div style={{position:"absolute",bottom:-16,right:-16,width:70,height:70,borderRadius:"50%",
              background:`radial-gradient(circle,${clr}18,transparent 70%)`,pointerEvents:"none"}}/>
            <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start",marginBottom:10}}>
              <span style={{fontSize:9,color:"#546190",fontWeight:700,letterSpacing:.8,textTransform:"uppercase"}}>{label}</span>
              <div style={{width:26,height:26,borderRadius:7,background:`${clr}14`,border:`1px solid ${clr}20`,
                display:"flex",alignItems:"center",justifyContent:"center"}}>
                <Icon size={12} color={clr} strokeWidth={2}/>
              </div>
            </div>
            <div style={{fontSize:15,fontWeight:800,color:clr===G?G:"#E8EAF6",letterSpacing:"-.3px",lineHeight:1,marginBottom:5}}>{val}</div>
            <div style={{fontSize:10,color:"#546190",fontWeight:500}}>{sub}</div>
          </div>
        ))}
      </div>

      {/* ── Chart ── */}
      <div style={{borderRadius:14,padding:"16px",
        background:"rgba(8,11,26,0.72)",border:"1px solid rgba(201,168,76,0.12)",backdropFilter:"blur(18px)"}}>
        <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:14}}>
          <div>
            <div style={{fontSize:13,fontWeight:700,color:"#E8EAF6",marginBottom:2}}>Performance</div>
            <div style={{fontSize:10,color:"#546190"}}>30-day portfolio history</div>
          </div>
          <div style={{display:"flex",gap:4,background:"rgba(120,140,200,0.07)",borderRadius:8,padding:3,
            border:"1px solid rgba(120,140,200,0.10)"}}>
            {["portfolio","btc","eth"].map(t => (
              <button key={t} onClick={() => setTab(t)} style={{
                padding:"4px 9px",borderRadius:6,border:"none",cursor:"pointer",fontSize:10,fontWeight:700,
                background:tab===t?"rgba(201,168,76,0.15)":"transparent",
                color:tab===t?G:"#546190",
                boxShadow:tab===t?`0 0 8px ${G}20`:"none",
                transition:"all .15s"}}>
                {t==="portfolio"?"Portfolio":t.toUpperCase()}
              </button>
            ))}
          </div>
        </div>
        <ResponsiveContainer width="100%" height={160}>
          <AreaChart data={CHART} margin={{top:4,right:0,left:-28,bottom:0}}>
            <defs>
              <linearGradient id="dashGrad" x1="0" y1="0" x2="0" y2="1">
                <stop offset="0%" stopColor={lineClr} stopOpacity={.25}/>
                <stop offset="100%" stopColor={lineClr} stopOpacity={0}/>
              </linearGradient>
            </defs>
            <CartesianGrid strokeDasharray="4 4" stroke="rgba(120,140,200,0.05)" vertical={false}/>
            <XAxis dataKey="d" tick={{fill:"#3D4F7C",fontSize:9}} tickLine={false} axisLine={false} interval={2}/>
            <YAxis tick={{fill:"#3D4F7C",fontSize:9}} tickLine={false} axisLine={false}
              tickFormatter={v=>`$${(v/1000).toFixed(0)}k`}/>
            <Tooltip content={<Tip/>}/>
            <Area type="monotone" dataKey="v" stroke={lineClr} strokeWidth={2}
              fill="url(#dashGrad)" dot={false}
              activeDot={{r:4,fill:lineClr,stroke:"#080B14",strokeWidth:2}}/>
          </AreaChart>
        </ResponsiveContainer>
      </div>

      {/* ── Live Prices ── */}
      <div style={{borderRadius:14,padding:"14px 16px",
        background:"rgba(8,11,26,0.72)",border:"1px solid rgba(120,140,200,0.12)",backdropFilter:"blur(18px)"}}>
        <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:12}}>
          <span style={{fontSize:13,fontWeight:700,color:"#E8EAF6"}}>Live Prices</span>
          <div style={{display:"flex",alignItems:"center",gap:5}}>
            <div style={{width:5,height:5,borderRadius:"50%",background:G,
              boxShadow:`0 0 6px ${G}`,animation:"blink 2s infinite"}}/>
            <span style={{fontSize:9,fontWeight:700,color:G,letterSpacing:.5}}>LIVE</span>
          </div>
        </div>
        <div style={{display:"flex",flexDirection:"column",gap:8}}>
          {Object.values(COINS).map(c => {
            const sym = c.name==="Bitcoin"?"BTC":c.name==="Ethereum"?"ETH":"USDT";
            return (
              <div key={c.name} style={{
                display:"flex",alignItems:"center",gap:12,padding:"10px 12px",
                borderRadius:10,
                background:"rgba(120,140,200,0.04)",
                border:"1px solid rgba(120,140,200,0.09)",
                transition:"background .15s",cursor:"default"
              }}
                onMouseEnter={e=>e.currentTarget.style.background="rgba(201,168,76,0.05)"}
                onMouseLeave={e=>e.currentTarget.style.background="rgba(120,140,200,0.04)"}
              >
                <div style={{width:32,height:32,borderRadius:9,background:`${c.clr}14`,
                  border:`1px solid ${c.clr}22`,display:"flex",alignItems:"center",justifyContent:"center",
                  fontSize:14,color:c.clr,fontWeight:900,flexShrink:0}}>{c.sym}</div>
                <div style={{flex:1}}>
                  <div style={{fontSize:12,fontWeight:700,color:"#E8EAF6"}}>{c.name}</div>
                  <div style={{fontSize:10,color:"#546190"}}>{sym}</div>
                </div>
                <div style={{textAlign:"right"}}>
                  <div style={{fontSize:13,fontWeight:800,color:"#E8EAF6",fontVariantNumeric:"tabular-nums"}}>
                    {c.px>=1000?`$${c.px.toLocaleString("en-US",{minimumFractionDigits:2,maximumFractionDigits:2})}`:
                      `$${c.px.toFixed(4)}`}
                  </div>
                  <div style={{display:"flex",alignItems:"center",gap:3,justifyContent:"flex-end",marginTop:2,
                    color:c.ch>=0?"#4ADE80":"#F87171",fontSize:10,fontWeight:700}}>
                    {c.ch>=0?<TrendingUp size={9}/>:<TrendingDown size={9}/>}
                    {c.ch>=0?"+":""}{c.ch.toFixed(2)}%
                  </div>
                </div>
              </div>
            );
          })}
        </div>
      </div>

      {/* ── Portfolio Ring Widget ── */}
      <DashboardRing txns={txns} now={now} go={go}/>

      {/* ── Total Distribution Banner ── */}
      <DistributionBanner txns={txns} now={now}/>

      {/* ── Recent Transactions preview ── */}
      <div style={{borderRadius:14,padding:"14px 16px",
        background:"rgba(8,11,26,0.72)",border:"1px solid rgba(120,140,200,0.12)",backdropFilter:"blur(18px)"}}>
        <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",marginBottom:12}}>
          <span style={{fontSize:13,fontWeight:700,color:"#E8EAF6"}}>Recent Activity</span>
          <button onClick={()=>go("transactions")} style={{fontSize:10,color:G,background:"none",
            border:"none",cursor:"pointer",fontWeight:600,display:"flex",alignItems:"center",gap:3}}>
            View all <ChevronRight size={11}/>
          </button>
        </div>

        {txns.length === 0 ? (
          <div style={{textAlign:"center",padding:"20px 0"}}>
            <div style={{width:40,height:40,borderRadius:11,background:"rgba(120,140,200,0.06)",
              border:"1px solid rgba(120,140,200,0.10)",
              display:"flex",alignItems:"center",justifyContent:"center",margin:"0 auto 10px"}}>
              <Activity size={18} color="#3D4F7C" strokeWidth={1.5}/>
            </div>
            <p style={{margin:"0 0 4px",fontSize:12,fontWeight:600,color:"#546190"}}>No activity yet</p>
            <p style={{margin:"0 0 14px",fontSize:11,color:"#3D4F7C"}}>Choose a plan to start earning</p>
            <button onClick={()=>go("plans")} style={{display:"inline-flex",alignItems:"center",gap:6,
              padding:"8px 16px",borderRadius:9,background:`linear-gradient(135deg,${G},${GD})`,
              border:"none",color:"#000",fontSize:12,fontWeight:800,cursor:"pointer"}}>
              <Star size={12}/> View Plans
            </button>
          </div>
        ) : txns.slice(0,2).map(tx => {
          const secs = (now - tx.timestamp)/1000;
          const profit = tx.usdValue*(tx.planDaily/100)*(secs/86400);
          return (
            <div key={tx.id} style={{display:"flex",alignItems:"center",gap:12,padding:"10px 0",
              borderBottom:"1px solid rgba(120,140,200,0.08)"}}>
              <div style={{width:34,height:34,borderRadius:9,flexShrink:0,
                background:"rgba(201,168,76,0.10)",border:"1px solid rgba(201,168,76,0.20)",
                display:"flex",alignItems:"center",justifyContent:"center",
                fontSize:11,fontWeight:800,color:G}}>{tx.coin}</div>
              <div style={{flex:1,minWidth:0}}>
                <div style={{fontSize:12,fontWeight:700,color:"#E8EAF6"}}>{tx.plan} Plan</div>
                <div style={{fontSize:10,color:"#546190"}}>{tx.planDaily}%/day · {tx.amount} {tx.coin}</div>
              </div>
              <div style={{textAlign:"right",flexShrink:0}}>
                <div style={{fontSize:12,fontWeight:800,color:G}}>+${profit.toFixed(4)}</div>
                <div style={{fontSize:9,color:"#3D4F7C"}}>live profit</div>
              </div>
            </div>
          );
        })}
      </div>

      <style>{`
        @keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}
        @keyframes blink{0%,100%{opacity:1}50%{opacity:.25}}
      `}</style>
    </div>
  );
}

/* Stable input style — outside components so never recreated on render */
const FORM_INP = {
  width:"100%", padding:"10px 12px", borderRadius:9,
  background:"rgba(8,10,25,0.65)", border:"1px solid rgba(120,140,200,0.18)",
  color:"#E8EAF6", fontSize:14, outline:"none",
  boxSizing:"border-box", fontFamily:"inherit", transition:"border-color .18s",
};
const FORM_INP_LIGHT = {
  ...FORM_INP,
  background:"rgba(235,237,250,0.95)", border:"1px solid rgba(100,120,200,0.22)",
  color:"#0D1130",
};

/* ═══ DEPOSIT ═══ */
function Deposit({ COINS, selectedPlan, onTxSubmit, go }) {
  const { dark, T } = useTheme();
  const inp = dark ? FORM_INP : FORM_INP_LIGHT;
  const [tab, setTab]           = useState("BTC");
  const [usdtNet, setUsdtNet]   = useState(0);
  const [copied, setCopied]     = useState(false);
  const [hash, setHash]         = useState("");
  const [amt, setAmt]           = useState("");
  const [done, setDone]         = useState(false);
  const [err, setErr]           = useState("");

  // Refs so submit always reads the latest values — no stale closure
  const hashRef = useRef("");
  const amtRef  = useRef("");

  const updateHash = (v) => { setHash(v); hashRef.current = v; setErr(""); };
  const updateAmt  = (v) => { setAmt(v);  amtRef.current  = v; setErr(""); };

  const base = COINS[tab];
  const activeNetwork = tab === "USDT" && base.networks ? base.networks[usdtNet] : null;
  const activeAddr    = activeNetwork ? activeNetwork.addr : base.addr;
  const activeNet     = activeNetwork ? activeNetwork.name : base.net;

  const copy = () => {
    navigator.clipboard?.writeText(activeAddr).catch(()=>{});
    setCopied(true); setTimeout(()=>setCopied(false), 2000);
  };

  const submit = () => {
    const h = hashRef.current.trim();
    const a = amtRef.current.trim();
    if (!h) { setErr("Please paste your transaction hash / TXID."); return; }
    if (!a || parseFloat(a) <= 0) { setErr("Please enter the amount you sent."); return; }
    const usdValue = parseFloat(a) * base.px;
    const plan = selectedPlan || PLANS[0];
    onTxSubmit({
      id:        Date.now(),
      coin:      tab,
      amount:    parseFloat(a),
      usdValue,
      hash:      h,
      plan:      plan.name,
      planDaily: plan.daily,
      planId:    plan.id,
      timestamp: Date.now(),
      network:   activeNet,
    });
    setDone(true);
    setHash(""); setAmt(""); hashRef.current=""; amtRef.current=""; setErr("");
    setTimeout(() => { setDone(false); go("transactions"); }, 1800);
  };

  return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:12,boxSizing:"border-box"}}>

      {/* selected plan banner */}
      {selectedPlan && (
        <div style={{padding:"12px 14px",borderRadius:10,
          background:`linear-gradient(135deg,${selectedPlan.clr}12,${selectedPlan.clr}04)`,
          border:`1px solid ${selectedPlan.clr}30`,
          display:"flex",alignItems:"center",gap:12}}>
          <span style={{fontSize:20}}>{selectedPlan.icon}</span>
          <div style={{flex:1}}>
            <div style={{fontSize:12,fontWeight:700,color:selectedPlan.clr}}>{selectedPlan.name} Plan Selected</div>
            <div style={{fontSize:11,color:"#546190",marginTop:2}}>{selectedPlan.daily}% daily returns · Min ${selectedPlan.min.toLocaleString()}</div>
          </div>
          <button onClick={()=>go("plans")} style={{fontSize:10,color:"#546190",background:"none",border:"none",cursor:"pointer",fontWeight:600}}>Change</button>
        </div>
      )}
      <div style={{display:"flex",gap:6,background:"#0E1225",borderRadius:12,padding:5,border:"1px solid rgba(120,140,200,0.12)",width:"fit-content"}}>
        {Object.entries(COINS).map(([k,cr]) => (
          <button key={k} onClick={()=>setTab(k)} style={{
            padding:"8px 20px",borderRadius:9,border:"none",cursor:"pointer",fontWeight:700,fontSize:13,
            background:tab===k?"#131829":"transparent",color:tab===k?"#E8EAF6":"#546190",
            boxShadow:tab===k?"0 2px 6px rgba(0,0,0,.4)":"none",transition:"all .15s"}}>
            <span style={{color:cr.clr,marginRight:5}}>{cr.sym}</span>{k}
          </button>
        ))}
      </div>
      <Card style={{padding:"16px",display:"flex",flexDirection:"column",alignItems:"center",gap:12}}>
        <div style={{padding:12,borderRadius:14,background:"#fff",boxShadow:`0 0 0 4px ${base.clr}22, 0 10px 32px rgba(0,0,0,.5)`}}>
          <QR val={activeAddr} size={160}/>
        </div>

        {/* Network label — multichain selector for USDT */}
        {tab === "USDT" && base.networks ? (
          <div style={{width:"100%"}}>
            <div style={{fontSize:9,color:T.textSub,fontWeight:700,letterSpacing:.8,
              textTransform:"uppercase",marginBottom:7,textAlign:"center"}}>
              Select Network
            </div>
            <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:8}}>
              {base.networks.map((n,i)=>(
                <button key={i} onClick={()=>{setUsdtNet(i);setCopied(false);}} style={{
                  padding:"7px 4px",borderRadius:8,border:"none",cursor:"pointer",
                  fontWeight:700,fontSize:10,textAlign:"center",
                  background:usdtNet===i?`${n.clr}20`:(dark?"rgba(120,140,200,0.06)":"rgba(0,0,0,0.05)"),
                  color:usdtNet===i?n.clr:T.textSub,
                  boxShadow:usdtNet===i?`inset 0 0 0 1.5px ${n.clr}50`:`inset 0 0 0 1px ${T.borderSub}`,
                  transition:"all .15s",
                }}>
                  {n.label}
                </button>
              ))}
            </div>
            <div style={{marginTop:8,padding:"5px 10px",borderRadius:7,textAlign:"center",
              background:`${activeNetwork?.clr||G}12`,border:`1px solid ${activeNetwork?.clr||G}25`}}>
              <span style={{fontSize:10,fontWeight:700,color:activeNetwork?.clr||G}}>
                {activeNet}
              </span>
            </div>
          </div>
        ) : (
          <span style={{padding:"4px 14px",borderRadius:999,background:`${base.clr}16`,
            border:`1px solid ${base.clr}30`,color:base.clr,fontSize:12,fontWeight:700}}>
            {activeNet}
          </span>
        )}

        <p style={{margin:0,fontSize:13,color:T.textSub,textAlign:"center",lineHeight:1.8}}>
          Only send <strong style={{color:T.text}}>{tab}</strong> via <strong style={{color:T.text}}>{activeNet}</strong>. Sending via wrong network will result in permanent loss.
        </p>
        <div style={{width:"100%",padding:"11px 13px",borderRadius:11,
          background:dark?"rgba(8,10,25,0.80)":"rgba(235,237,250,0.95)",
          border:`1px solid ${T.borderSub}`,display:"flex",alignItems:"center",gap:10}}>
          <span style={{flex:1,fontSize:11,color:T.textSub,fontFamily:"monospace",
            overflow:"hidden",textOverflow:"ellipsis",whiteSpace:"nowrap"}}>{activeAddr}</span>
          <button onClick={copy} style={{display:"flex",alignItems:"center",gap:5,padding:"6px 11px",
            borderRadius:8,background:copied?`${G}12`:"rgba(120,140,200,0.10)",
            border:copied?`1px solid ${G}30`:"1px solid rgba(120,140,200,0.15)",
            color:copied?G:T.textSub,fontSize:11,fontWeight:700,cursor:"pointer",flexShrink:0,transition:"all .2s"}}>
            {copied?<Check size={11}/>:<Copy size={11}/>} {copied?"Copied":"Copy"}
          </button>
        </div>
        <div style={{width:"100%",padding:"12px 14px",borderRadius:11,background:"rgba(251,191,36,.05)",border:"1px solid rgba(251,191,36,.18)",display:"flex",alignItems:"flex-start",gap:10}}>
          <AlertTriangle size={14} color="#FBBF24" style={{flexShrink:0,marginTop:1}}/>
          <span style={{fontSize:12,color:"#8B6A10",lineHeight:1.8}}>Always verify the address before sending. Crypto transactions are irreversible.</span>
        </div>
      </Card>
      <Card style={{padding:"14px"}}>
        <h3 style={{margin:"0 0 18px",fontSize:13,fontWeight:700,color:"#E8EAF6",letterSpacing:"-.3px"}}>Confirm Deposit</h3>
        <div style={{display:"flex",flexDirection:"column",gap:14}}>
          <div>
            <label style={{fontSize:10,color:"#546190",display:"block",marginBottom:7,fontWeight:700,letterSpacing:.8,textTransform:"uppercase"}}>Transaction Hash / TXID</label>
            <input value={hash} onChange={e=>updateHash(e.target.value)} placeholder="Paste transaction hash…"
              style={{...inp,fontFamily:"monospace",fontSize:12}}
              onFocus={e=>e.target.style.borderColor='rgba(201,168,76,0.45)'}
              onBlur={e=>e.target.style.borderColor="rgba(120,140,200,0.13)"}/>
          </div>
          <div>
            <label style={{fontSize:10,color:"#546190",display:"block",marginBottom:7,fontWeight:700,letterSpacing:.8,textTransform:"uppercase"}}>Amount ({tab})</label>
            <div style={{position:"relative"}}>
              <input value={amt} onChange={e=>updateAmt(e.target.value)} placeholder="0.00" type="number"
                style={{...inp,fontSize:15,fontWeight:700,paddingRight:64}}
                onFocus={e=>e.target.style.borderColor='rgba(201,168,76,0.45)'}
                onBlur={e=>e.target.style.borderColor="rgba(120,140,200,0.13)"}/>
              <span style={{position:"absolute",right:13,top:"50%",transform:"translateY(-50%)",fontSize:12,color:base.clr,fontWeight:800}}>{tab}</span>
            </div>
            {amt && <p style={{margin:"5px 0 0",fontSize:11,color:"#546190"}}>
              ≈ ${(parseFloat(amt||0)*base.px).toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})} USD
            </p>}
          </div>
          {err && (
            <div style={{padding:"9px 13px",borderRadius:9,
              background:"rgba(248,113,113,0.08)",border:"1px solid rgba(248,113,113,0.25)",
              fontSize:12,color:"#F87171",display:"flex",alignItems:"center",gap:7}}>
              <AlertTriangle size={13}/> {err}
            </div>
          )}
          <button onClick={submit} style={{padding:"10px",borderRadius:9,border:"none",
            background:done?"linear-gradient(135deg,#059669,#047857)":`linear-gradient(135deg,${G},${GD})`,
            color:"#000",fontWeight:800,fontSize:14,cursor:"pointer",
            display:"flex",alignItems:"center",justifyContent:"center",gap:8,
            transition:"all .25s",boxShadow:done?"none":`0 4px 18px ${G}28`}}>
            {done?<><CheckCircle2 size={16}/> Submitted!</>:"Submit Transaction"}
          </button>
        </div>
      </Card>
      <Card style={{padding:"14px"}}>
        <h4 style={{margin:"0 0 14px",fontSize:12,fontWeight:600,color:"#E8EAF6"}}>How to deposit</h4>
        {[
          {n:1,t:"Copy the wallet address",d:"Use the copy button or scan the QR code."},
          {n:2,t:`Send ${tab} from your wallet`,d:"Initiate the transfer from your external wallet."},
          {n:3,t:"Submit the transaction hash",d:"Paste your TXID above once sent."},
          {n:4,t:"Funds credited automatically",d:"Balance updates after 1–3 confirmations."},
        ].map(({n,t,d}) => (
          <div key={n} style={{display:"flex",gap:12,alignItems:"flex-start",marginBottom:12}}>
            <div style={{width:24,height:24,borderRadius:7,flexShrink:0,background:`${G}10`,border:`1px solid ${G}22`,
              display:"flex",alignItems:"center",justifyContent:"center",fontSize:11,fontWeight:800,color:G}}>{n}</div>
            <div>
              <div style={{fontSize:13,fontWeight:700,color:"#E8EAF6",marginBottom:2}}>{t}</div>
              <div style={{fontSize:11,color:"#546190",lineHeight:1.7}}>{d}</div>
            </div>
          </div>
        ))}
      </Card>
    </div>
  );
}


/* ═══ WITHDRAW ═══ */
function Withdraw({ COINS, txns }) {
  const { dark, T } = useTheme();
  const inp = dark ? FORM_INP : FORM_INP_LIGHT;

  const [tab,     setTab]     = useState("withdraw"); // "withdraw" | "history"
  const [sel,     setSel]     = useState("BTC");
  const [amt,     setAmt]     = useState("");
  const [addr,    setAddr]    = useState("");
  const [done,    setDone]    = useState(false);
  const [err,     setErr]     = useState("");
  const [wHistory,setWHistory]= useState(() => {
    try { return JSON.parse(localStorage.getItem("aetherlink_withdrawals")||"[]"); } catch { return []; }
  });
  const [now, setNow] = useState(Date.now());
  useEffect(() => {
    const id = setInterval(() => setNow(Date.now()), 1000);
    return () => clearInterval(id);
  }, []);

  // Compute live balances from txns
  const balances = { BTC: 0, ETH: 0, USDT: 0 };
  const profits  = { BTC: 0, ETH: 0, USDT: 0 };
  txns.forEach(t => {
    const coin = t.coin;
    if (balances[coin] !== undefined) {
      const secs   = (now - t.timestamp) / 1000;
      const profit = t.usdValue * (t.planDaily / 100) * (secs / 86400);
      const profitInCoin = profit / (COINS[coin]?.px || 1);
      balances[coin] += t.amount;
      profits[coin]  += profitInCoin;
    }
  });
  const totalBal  = Object.entries(balances).reduce((s,[k,v]) => s + v*(COINS[k]?.px||0), 0);
  const totalProfit = Object.entries(profits).reduce((s,[k,v]) => s + v*(COINS[k]?.px||0), 0);
  const withdrawable = profits[sel] || 0;
  const withdrawableUSD = withdrawable * (COINS[sel]?.px || 1);

  const setMax = () => setAmt(withdrawable.toFixed(sel === "USDT" ? 4 : 8));

  const submit = () => {
    setErr("");
    const n = parseFloat(amt);
    if (!amt || isNaN(n) || n <= 0) { setErr("Please enter a valid amount."); return; }
    if (n > withdrawable) { setErr(`Insufficient balance. Max: ${withdrawable.toFixed(6)} ${sel}`); return; }
    if (!addr.trim()) { setErr("Please enter your wallet address."); return; }

    const record = {
      id:        Date.now(),
      coin:      sel,
      amount:    n,
      usdValue:  n * (COINS[sel]?.px || 1),
      addr:      addr,
      timestamp: Date.now(),
      status:    "Pending",
    };
    const next = [record, ...wHistory];
    setWHistory(next);
    try { localStorage.setItem("aetherlink_withdrawals", JSON.stringify(next)); } catch {}
    setDone(true);
    setAmt(""); setAddr("");
    setTimeout(() => { setDone(false); setTab("history"); }, 1800);
  };

  const coin = COINS[sel];
  const totalProfitUSD = Object.entries(profits)
    .reduce((s,[k,v]) => s + v*(COINS[k]?.px||0), 0);

  return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:12,boxSizing:"border-box"}}>

      {/* ── Top balance overview ── */}
      <div style={{
        borderRadius:16, padding:"18px 16px",
        background: dark
          ? "linear-gradient(135deg,rgba(201,168,76,0.10) 0%,rgba(124,111,205,0.06) 100%)"
          : "linear-gradient(135deg,rgba(201,168,76,0.15) 0%,rgba(255,255,255,0.90) 100%)",
        border:`1px solid ${dark?"rgba(201,168,76,0.22)":"rgba(201,168,76,0.35)"}`,
        backdropFilter:"blur(20px)",
        position:"relative", overflow:"hidden",
      }}>
        <div style={{position:"absolute",top:0,left:0,right:0,height:1,
          background:"linear-gradient(90deg,transparent,rgba(201,168,76,0.6),transparent)",
          backgroundSize:"200% 100%",animation:"shimmer 2.5s linear infinite"}}/>

        <div style={{fontSize:9,color:G,fontWeight:700,letterSpacing:1.5,textTransform:"uppercase",marginBottom:8}}>
          Available to Withdraw
        </div>
        <div style={{
          fontSize:28, fontWeight:900, letterSpacing:"-1px",
          background:`linear-gradient(135deg,${G2},${G})`,
          WebkitBackgroundClip:"text", WebkitTextFillColor:"transparent",
          marginBottom:4,
        }}>
          ${totalProfitUSD.toFixed(4)}
        </div>
        <div style={{fontSize:11,color:T.textSub,marginBottom:14}}>
          Live profit from your investments
        </div>

        {/* Coin profit cards */}
        <div style={{display:"grid",gridTemplateColumns:"repeat(3,1fr)",gap:8}}>
          {["BTC","ETH","USDT"].map(k => {
            const c = COINS[k];
            const p = profits[k] || 0;
            const pUSD = p * (c?.px||1);
            return (
              <div key={k} onClick={()=>setSel(k)} style={{
                padding:"10px",borderRadius:10,cursor:"pointer",
                background: sel===k
                  ? `${c?.clr||G}18`
                  : dark?"rgba(255,255,255,0.04)":"rgba(255,255,255,0.60)",
                border: sel===k ? `1px solid ${c?.clr||G}40` : `1px solid ${T.borderSub}`,
                transition:"all .2s",
              }}>
                <div style={{display:"flex",alignItems:"center",gap:6,marginBottom:6}}>
                  <div style={{width:22,height:22,borderRadius:6,
                    background:`${c?.clr||G}18`,border:`1px solid ${c?.clr||G}22`,
                    display:"flex",alignItems:"center",justifyContent:"center",
                    fontSize:11,color:c?.clr||G,fontWeight:900}}>{c?.sym}</div>
                  <span style={{fontSize:10,fontWeight:700,color:T.text}}>{k}</span>
                </div>
                <div style={{fontSize:11,fontWeight:800,color:G,marginBottom:2,fontVariantNumeric:"tabular-nums"}}>
                  +{p.toFixed(6)}
                </div>
                <div style={{fontSize:9,color:T.textSub}}>${pUSD.toFixed(4)}</div>
              </div>
            );
          })}
        </div>
      </div>

      {/* ── Tab switcher ── */}
      <div style={{display:"flex",gap:4,background:dark?"rgba(120,140,200,0.05)":"rgba(0,0,0,0.05)",
        borderRadius:10,padding:4,border:`1px solid ${T.borderSub}`}}>
        {[["withdraw","💸 Withdraw"],["history","📋 History"]].map(([id,label])=>(
          <button key={id} onClick={()=>setTab(id)} style={{
            flex:1,padding:"8px",borderRadius:8,border:"none",cursor:"pointer",
            fontWeight:700,fontSize:12,transition:"all .15s",
            background:tab===id ? `linear-gradient(135deg,${G},${GD})` : "transparent",
            color:tab===id?"#000":T.textSub,
            boxShadow:tab===id?`0 2px 8px ${G}30`:"none",
          }}>{label}</button>
        ))}
      </div>

      {/* ── WITHDRAW TAB ── */}
      {tab === "withdraw" && (
        <>
          <Card style={{padding:"18px"}}>
            <h3 style={{margin:"0 0 14px",fontSize:13,fontWeight:700,color:T.text}}>
              Withdrawal Request
            </h3>

            {/* Coin selector */}
            <div style={{marginBottom:12}}>
              <label style={{fontSize:9,color:T.textSub,display:"block",marginBottom:6,
                fontWeight:700,letterSpacing:.8,textTransform:"uppercase"}}>Cryptocurrency</label>
              <div style={{display:"flex",gap:6}}>
                {["BTC","ETH","USDT"].map(k => {
                  const c = COINS[k];
                  return (
                    <button key={k} onClick={()=>{setSel(k);setAmt("");setErr("");}} style={{
                      flex:1,padding:"9px 0",borderRadius:8,border:"none",cursor:"pointer",
                      fontWeight:700,fontSize:12,
                      background:sel===k?`${c.clr}18`:dark?"rgba(120,140,200,0.07)":"rgba(0,0,0,0.05)",
                      color:sel===k?c.clr:T.textSub,
                      boxShadow:sel===k?`inset 0 0 0 1px ${c.clr}35`:`inset 0 0 0 1px ${T.borderSub}`,
                      transition:"all .15s",
                    }}>
                      {c.sym} {k}
                    </button>
                  );
                })}
              </div>
            </div>

            {/* Withdrawable balance info */}
            <div style={{padding:"10px 12px",borderRadius:9,marginBottom:12,
              background:dark?"rgba(201,168,76,0.06)":"rgba(201,168,76,0.08)",
              border:`1px solid ${G}22`,
              display:"flex",justifyContent:"space-between",alignItems:"center"}}>
              <div>
                <div style={{fontSize:9,color:T.textSub,marginBottom:3,letterSpacing:.5,textTransform:"uppercase"}}>
                  Available Profit
                </div>
                <div style={{fontSize:14,fontWeight:800,color:G,fontVariantNumeric:"tabular-nums"}}>
                  {withdrawable.toFixed(8)} {sel}
                </div>
                <div style={{fontSize:10,color:T.textSub}}>${withdrawableUSD.toFixed(4)} USD</div>
              </div>
              <button onClick={setMax} style={{
                padding:"6px 12px",borderRadius:7,border:`1px solid ${G}30`,
                background:`${G}12`,color:G,fontSize:11,fontWeight:800,cursor:"pointer",
              }}>MAX</button>
            </div>

            {/* Amount input */}
            <div style={{marginBottom:12}}>
              <label style={{fontSize:9,color:T.textSub,display:"block",marginBottom:6,
                fontWeight:700,letterSpacing:.8,textTransform:"uppercase"}}>Amount ({sel})</label>
              <div style={{position:"relative"}}>
                <input
                  value={amt}
                  onChange={e=>{setAmt(e.target.value);setErr("");}}
                  placeholder="0.00000000"
                  type="number"
                  step="any"
                  style={{...inp,fontSize:16,fontWeight:800,paddingRight:60}}
                  onFocus={e=>e.target.style.borderColor=`${G}50`}
                  onBlur={e=>e.target.style.borderColor=dark?"rgba(120,140,200,0.18)":"rgba(100,120,200,0.22)"}
                />
                <span style={{position:"absolute",right:12,top:"50%",transform:"translateY(-50%)",
                  fontSize:11,color:coin?.clr||G,fontWeight:800}}>{sel}</span>
              </div>
              {amt && (
                <div style={{fontSize:10,color:T.textSub,marginTop:4}}>
                  ≈ ${(parseFloat(amt||0)*(coin?.px||1)).toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})} USD
                </div>
              )}
            </div>

            {/* Address input */}
            <div style={{marginBottom:14}}>
              <label style={{fontSize:9,color:T.textSub,display:"block",marginBottom:6,
                fontWeight:700,letterSpacing:.8,textTransform:"uppercase"}}>Destination Address</label>
              <input
                value={addr}
                onChange={e=>{setAddr(e.target.value);setErr("");}}
                placeholder={`Enter your ${sel} wallet address…`}
                style={{...inp,fontFamily:"monospace",fontSize:11}}
                onFocus={e=>e.target.style.borderColor=`${G}50`}
                onBlur={e=>e.target.style.borderColor=dark?"rgba(120,140,200,0.18)":"rgba(100,120,200,0.22)"}
              />
            </div>

            {err && (
              <div style={{padding:"9px 12px",borderRadius:9,marginBottom:12,
                background:"rgba(248,113,113,0.08)",border:"1px solid rgba(248,113,113,0.25)",
                fontSize:12,color:"#F87171",display:"flex",alignItems:"center",gap:7}}>
                <AlertTriangle size={13}/> {err}
              </div>
            )}

            <button onClick={submit} style={{
              width:"100%",padding:"13px",borderRadius:10,border:"none",
              background:done
                ? "linear-gradient(135deg,#059669,#047857)"
                : "linear-gradient(135deg,#9333EA,#7C3AED)",
              color:"#fff",fontWeight:800,fontSize:13,cursor:"pointer",
              display:"flex",alignItems:"center",justifyContent:"center",gap:8,
              transition:"all .25s",
              boxShadow:done?"none":"0 4px 18px rgba(147,51,234,.30)",
            }}>
              {done
                ? <><CheckCircle2 size={15}/> Request Submitted!</>
                : <><ArrowUpFromLine size={14}/> Request Withdrawal</>
              }
            </button>
          </Card>

          {/* Info cards */}
          <Card style={{padding:"14px 16px"}}>
            <div style={{display:"flex",alignItems:"center",gap:8,marginBottom:8}}>
              <Clock size={13} color="#60A5FA"/>
              <span style={{fontSize:12,fontWeight:700,color:T.text}}>Processing Time</span>
            </div>
            <p style={{margin:0,fontSize:11,color:T.textSub,lineHeight:1.7}}>
              Withdrawal requests are reviewed within <strong style={{color:T.text}}>24–48 hours</strong>. You'll receive a notification once approved and processed.
            </p>
          </Card>

          <Card style={{padding:"14px 16px"}}>
            <div style={{display:"flex",alignItems:"center",gap:8,marginBottom:8}}>
              <Shield size={13} color={G}/>
              <span style={{fontSize:12,fontWeight:700,color:T.text}}>Withdrawal Policy</span>
            </div>
            <div style={{display:"flex",flexDirection:"column",gap:6}}>
              {[
                "Only live profits are withdrawable",
                "Minimum withdrawal: $10 USD equivalent",
                "Original deposit remains active in your plan",
                "Withdrawals are irreversible once broadcast",
              ].map((t,i)=>(
                <div key={i} style={{display:"flex",alignItems:"flex-start",gap:8}}>
                  <div style={{width:4,height:4,borderRadius:"50%",background:G,flexShrink:0,marginTop:5}}/>
                  <span style={{fontSize:11,color:T.textSub,lineHeight:1.6}}>{t}</span>
                </div>
              ))}
            </div>
          </Card>
        </>
      )}

      {/* ── HISTORY TAB ── */}
      {tab === "history" && (
        <>
          {wHistory.length === 0 ? (
            <Card style={{padding:"50px 20px",textAlign:"center"}}>
              <div style={{width:48,height:48,borderRadius:13,
                background:dark?"rgba(255,255,255,0.04)":"rgba(0,0,0,0.05)",
                border:`1px solid ${T.borderSub}`,
                display:"flex",alignItems:"center",justifyContent:"center",margin:"0 auto 14px"}}>
                <ArrowUpFromLine size={20} color={T.textMuted} strokeWidth={1.5}/>
              </div>
              <p style={{margin:"0 0 5px",fontSize:13,fontWeight:700,color:T.textSub}}>
                No withdrawals yet
              </p>
              <p style={{margin:"0 0 14px",fontSize:11,color:T.textMuted,lineHeight:1.7}}>
                Your withdrawal requests will appear here
              </p>
              <button onClick={()=>setTab("withdraw")} style={{
                padding:"8px 18px",borderRadius:9,border:`1px solid ${G}30`,
                background:`${G}10`,color:G,fontSize:12,fontWeight:700,cursor:"pointer",
              }}>
                Make a Withdrawal →
              </button>
            </Card>
          ) : (
            <div style={{display:"flex",flexDirection:"column",gap:10}}>
              {wHistory.map(w => (
                <Card key={w.id} style={{padding:"14px 16px",position:"relative",overflow:"hidden"}}>
                  <div style={{position:"absolute",top:0,left:0,right:0,height:2,
                    background:"linear-gradient(90deg,#9333EA,#7C3AED,transparent)",opacity:.7}}/>
                  <div style={{display:"flex",justifyContent:"space-between",alignItems:"flex-start",marginBottom:10}}>
                    <div>
                      <div style={{display:"flex",alignItems:"center",gap:7,marginBottom:4}}>
                        <div style={{width:26,height:26,borderRadius:7,
                          background:`${COINS[w.coin]?.clr||G}18`,
                          border:`1px solid ${COINS[w.coin]?.clr||G}25`,
                          display:"flex",alignItems:"center",justifyContent:"center",
                          fontSize:11,fontWeight:800,color:COINS[w.coin]?.clr||G}}>
                          {COINS[w.coin]?.sym}
                        </div>
                        <span style={{fontSize:13,fontWeight:700,color:T.text}}>{w.coin}</span>
                        <span style={{
                          padding:"2px 7px",borderRadius:999,fontSize:9,fontWeight:700,
                          background: w.status==="Pending"
                            ? "rgba(251,191,36,0.12)" : "rgba(74,222,128,0.12)",
                          color: w.status==="Pending" ? "#FBBF24" : "#4ADE80",
                          border: `1px solid ${w.status==="Pending"?"rgba(251,191,36,0.25)":"rgba(74,222,128,0.25)"}`,
                        }}>
                          ● {w.status}
                        </span>
                      </div>
                      <div style={{fontSize:9,color:T.textSub,fontFamily:"monospace"}}>
                        To: {w.addr.slice(0,18)}…
                      </div>
                    </div>
                    <div style={{textAlign:"right"}}>
                      <div style={{fontSize:13,fontWeight:800,color:"#A855F7",marginBottom:2}}>
                        -{w.amount.toFixed(6)} {w.coin}
                      </div>
                      <div style={{fontSize:10,color:T.textSub,marginBottom:2}}>
                        ${w.usdValue.toFixed(2)} USD
                      </div>
                      <div style={{fontSize:9,color:T.textMuted}}>
                        {new Date(w.timestamp).toLocaleDateString("en-US",{month:"short",day:"numeric"})} at {new Date(w.timestamp).toLocaleTimeString("en-US",{hour:"2-digit",minute:"2-digit"})}
                      </div>
                    </div>
                  </div>
                  <div style={{padding:"8px 10px",borderRadius:8,
                    background:"rgba(147,51,234,0.05)",border:"1px solid rgba(147,51,234,0.12)",
                    fontSize:10,color:T.textSub,lineHeight:1.6}}>
                    ⏱ Pending admin review — typically processed within 24–48 hours.
                  </div>
                </Card>
              ))}
            </div>
          )}
        </>
      )}

      <style>{`
        @keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}
      `}</style>
    </div>
  );
}

/* ═══ TRANSACTIONS ═══ */
function Transactions({ txns, onClear }) {
  const [now, setNow] = useState(Date.now());
  useEffect(() => {
    const id = setInterval(() => setNow(Date.now()), 1000);
    return () => clearInterval(id);
  }, []);

  if (!txns.length) {
    return (
      <div style={{padding:"14px"}}>
        <div style={{borderRadius:16,padding:"50px 20px",textAlign:"center",
          background:"rgba(8,11,26,0.72)",border:"1px solid rgba(201,168,76,0.10)",
          backdropFilter:"blur(18px)"}}>
          <div style={{width:52,height:52,borderRadius:14,
            background:"rgba(201,168,76,0.08)",border:"1px solid rgba(201,168,76,0.15)",
            display:"flex",alignItems:"center",justifyContent:"center",margin:"0 auto 14px"}}>
            <Activity size={22} color={G} strokeWidth={1.5}/>
          </div>
          <p style={{margin:"0 0 6px",fontSize:14,fontWeight:700,color:"#E8EAF6"}}>No transactions yet</p>
          <p style={{margin:0,fontSize:12,color:"#546190",lineHeight:1.7}}>
            Submit a deposit to see your live profit counting here.
          </p>
        </div>
      </div>
    );
  }

  return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:14}}>
      {/* summary bar */}
      {(() => {
        const totalDep = txns.reduce((s,t)=>s+t.usdValue,0);
        const totalProfit = txns.reduce((s,t)=>{
          const secs=(now-t.timestamp)/1000;
          return s+t.usdValue*(t.planDaily/100)*(secs/86400);
        },0);
        return (
          <div style={{borderRadius:14,padding:"14px 16px",
            background:"linear-gradient(135deg,rgba(201,168,76,0.10),rgba(124,111,205,0.06))",
            border:"1px solid rgba(201,168,76,0.22)",
            backdropFilter:"blur(18px)",
            display:"flex",alignItems:"center",justifyContent:"space-between",
            position:"relative",overflow:"hidden"}}>
            <div style={{position:"absolute",top:0,left:0,right:0,height:1,
              background:"linear-gradient(90deg,transparent,rgba(201,168,76,0.5),transparent)",
              backgroundSize:"200% 100%",animation:"shimmer 3s linear infinite"}}/>
            <div>
              <div style={{fontSize:9,color:G,fontWeight:700,letterSpacing:1.2,textTransform:"uppercase",marginBottom:4}}>
                Total Portfolio
              </div>
              <div style={{fontSize:22,fontWeight:900,letterSpacing:"-1px",
                background:`linear-gradient(135deg,${G2},${G})`,
                WebkitBackgroundClip:"text",WebkitTextFillColor:"transparent"}}>
                ${(totalDep+totalProfit).toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}
              </div>
            </div>
            <div style={{textAlign:"right"}}>
              <div style={{fontSize:9,color:"#546190",fontWeight:600,letterSpacing:.8,textTransform:"uppercase",marginBottom:4}}>
                Live Profit
              </div>
              <div style={{fontSize:18,fontWeight:800,color:G}}>+${totalProfit.toFixed(4)}</div>
              <button onClick={()=>{if(window.confirm("Clear all transaction history?")) onClear();}}
                style={{marginTop:8,fontSize:9,color:"rgba(248,113,113,0.6)",background:"none",border:"none",
                  cursor:"pointer",fontWeight:600,letterSpacing:.3}}>
                Clear History
              </button>
            </div>
          </div>
        );
      })()}

      {/* transaction cards */}
      {txns.map((tx) => {
        const secsElapsed = (now - tx.timestamp) / 1000;
        const dailyRate   = tx.planDaily / 100;
        const profit      = tx.usdValue * dailyRate * (secsElapsed / 86400);
        const total       = tx.usdValue + profit;
        const pct         = (profit / tx.usdValue) * 100;
        const hrs         = Math.floor(secsElapsed / 3600);
        const mins        = Math.floor((secsElapsed % 3600) / 60);
        const secs        = Math.floor(secsElapsed % 60);

        // find plan color
        const plan = PLANS.find(p => p.id === tx.planId);
        const planClr = plan?.clr || G;

        return (
          <div key={tx.id} style={{
            borderRadius:16,overflow:"hidden",
            background:"rgba(8,11,26,0.78)",
            border:`1px solid rgba(201,168,76,0.14)`,
            backdropFilter:"blur(20px)",
            position:"relative",
          }}>
            {/* top accent line */}
            <div style={{height:2,background:`linear-gradient(90deg,${planClr},${G2},transparent)`,opacity:.7}}/>

            {/* glow */}
            <div style={{position:"absolute",top:-30,right:-30,width:140,height:140,borderRadius:"50%",
              background:`radial-gradient(circle,${G}0C,transparent 70%)`,pointerEvents:"none"}}/>

            {/* header */}
            <div style={{padding:"14px 16px 12px",display:"flex",justifyContent:"space-between",alignItems:"flex-start"}}>
              <div>
                <div style={{display:"flex",alignItems:"center",gap:8,marginBottom:5}}>
                  <div style={{width:30,height:30,borderRadius:8,flexShrink:0,
                    background:`rgba(201,168,76,0.12)`,border:`1px solid ${G}25`,
                    display:"flex",alignItems:"center",justifyContent:"center",
                    fontSize:12,fontWeight:800,color:G}}>{tx.coin}</div>
                  <span style={{fontSize:14,fontWeight:800,color:"#E8EAF6",letterSpacing:"-.3px"}}>{tx.coin}</span>
                  <div style={{display:"flex",alignItems:"center",gap:4,
                    padding:"3px 8px",borderRadius:999,
                    background:"rgba(74,222,128,0.10)",border:"1px solid rgba(74,222,128,0.20)"}}>
                    <div style={{width:5,height:5,borderRadius:"50%",background:"#4ADE80",
                      boxShadow:"0 0 5px #4ADE80",animation:"blink 2s infinite"}}/>
                    <span style={{fontSize:9,fontWeight:800,color:"#4ADE80",letterSpacing:.5}}>ACTIVE</span>
                  </div>
                </div>
                <div style={{fontSize:10,color:"#546190",fontFamily:"monospace",letterSpacing:.3}}>
                  {tx.hash.slice(0,22)}…
                </div>
              </div>
              <div style={{textAlign:"right"}}>
                <div style={{display:"flex",alignItems:"center",gap:5,justifyContent:"flex-end",marginBottom:3}}>
                  <div style={{width:8,height:8,borderRadius:2,background:planClr,opacity:.8}}/>
                  <span style={{fontSize:11,fontWeight:700,color:planClr}}>{tx.plan}</span>
                </div>
                <div style={{fontSize:10,fontWeight:700,color:G,marginBottom:2}}>{tx.planDaily}%/day</div>
                <div style={{fontSize:9,color:"#3D4F7C"}}>
                  {new Date(tx.timestamp).toLocaleDateString("en-US",{month:"short",day:"numeric"})} at {new Date(tx.timestamp).toLocaleTimeString("en-US",{hour:"2-digit",minute:"2-digit"})}
                </div>
              </div>
            </div>

            {/* divider */}
            <div style={{height:"1px",background:"linear-gradient(90deg,transparent,rgba(201,168,76,0.15),transparent)",margin:"0 16px"}}/>

            {/* 3 metric cards */}
            <div style={{padding:"12px 16px 14px",display:"grid",gridTemplateColumns:"1fr 1fr 1fr",gap:10}}>
              {/* Deposited */}
              <div style={{padding:"12px",borderRadius:11,
                background:"rgba(120,140,200,0.05)",
                border:"1px solid rgba(120,140,200,0.12)"}}>
                <div style={{fontSize:8,color:"#546190",marginBottom:6,textTransform:"uppercase",
                  letterSpacing:.8,fontWeight:700}}>Deposited</div>
                <div style={{fontSize:14,fontWeight:800,color:"#E8EAF6",letterSpacing:"-.5px",marginBottom:3}}>
                  ${tx.usdValue.toLocaleString(undefined,{minimumFractionDigits:2,maximumFractionDigits:2})}
                </div>
                <div style={{fontSize:9,color:"#546190",fontWeight:500}}>
                  {tx.amount} {tx.coin}
                </div>
              </div>

              {/* Live Profit - highlighted */}
              <div style={{padding:"12px",borderRadius:11,
                background:`linear-gradient(135deg,rgba(201,168,76,0.10),rgba(201,168,76,0.04))`,
                border:`1px solid rgba(201,168,76,0.25)`,
                position:"relative",overflow:"hidden"}}>
                <div style={{position:"absolute",bottom:-10,right:-10,width:50,height:50,borderRadius:"50%",
                  background:`radial-gradient(circle,${G}20,transparent)`,pointerEvents:"none"}}/>
                <div style={{fontSize:8,color:G,marginBottom:6,textTransform:"uppercase",
                  letterSpacing:.8,fontWeight:700}}>Live Profit</div>
                <div style={{fontSize:14,fontWeight:900,color:G,letterSpacing:"-.5px",marginBottom:3,
                  textShadow:`0 0 12px ${G}60`}}>
                  +${profit.toFixed(4)}
                </div>
                <div style={{fontSize:9,color:"rgba(201,168,76,0.6)",fontWeight:600}}>
                  +{pct.toFixed(4)}%
                </div>
              </div>

              {/* Total */}
              <div style={{padding:"12px",borderRadius:11,
                background:"rgba(120,140,200,0.05)",
                border:"1px solid rgba(120,140,200,0.12)"}}>
                <div style={{fontSize:8,color:"#546190",marginBottom:6,textTransform:"uppercase",
                  letterSpacing:.8,fontWeight:700}}>Total</div>
                <div style={{fontSize:14,fontWeight:800,color:"#E8EAF6",letterSpacing:"-.5px",marginBottom:3}}>
                  ${total.toFixed(2)}
                </div>
                <div style={{fontSize:9,color:"#546190",fontWeight:500,fontVariantNumeric:"tabular-nums"}}>
                  {hrs}h {mins}m {secs}s
                </div>
              </div>
            </div>
          </div>
        );
      })}
      <style>{`
        @keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}
        @keyframes blink{0%,100%{opacity:1}50%{opacity:.25}}
      `}</style>
    </div>
  );
}

/* ═══ PLANS ═══ */
function Plans({ go, onSelectPlan, txns }) {
  return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:14}}>
      {/* ── section label ── */}
      <div style={{textAlign:"center",padding:"6px 0 2px"}}>
        <div style={{display:"inline-flex",alignItems:"center",gap:6,padding:"4px 12px",
          borderRadius:999,background:`${G}10`,border:`1px solid ${G}22`}}>
          <div style={{width:5,height:5,borderRadius:"50%",background:G,animation:"blink 2s infinite"}}/>
          <span style={{fontSize:9,fontWeight:700,color:G,letterSpacing:1.2,textTransform:"uppercase"}}>Live Investment Plans</span>
        </div>
        <h2 style={{margin:"8px 0 4px",fontSize:17,fontWeight:800,color:"#E8EAF6",letterSpacing:"-.5px"}}>
          Choose Your Plan
        </h2>
        <p style={{margin:0,fontSize:12,color:"#546190",lineHeight:1.6}}>
          Select a plan and start earning daily returns. Profits compound automatically.
        </p>
      </div>

      {/* ── plan cards ── */}
      {PLANS.map((plan) => {
        const isActive = txns.some(t => t.planId === plan.id);
        return (
          <div key={plan.id} style={{
            borderRadius:16,overflow:"hidden",
            border:`1px solid ${isActive ? plan.clr+"60" : plan.clr+"30"}`,
            background:`linear-gradient(135deg,${plan.glow} 0%,rgba(8,11,26,0.96) 65%)`,
            position:"relative",
            boxShadow: isActive ? `0 0 20px ${plan.clr}18` : "none",
          }}>
            {/* top accent */}
            <div style={{height:2,background:`linear-gradient(90deg,${plan.clr},${plan.clr}40,transparent)`,opacity:.8}}/>

            {plan.id === "gold" && (
              <div style={{position:"absolute",top:12,right:12,
                padding:"3px 10px",borderRadius:999,
                background:"linear-gradient(135deg,#FFD700,#FFA500)",
                fontSize:9,fontWeight:800,color:"#000",letterSpacing:.5}}>
                ⭐ POPULAR
              </div>
            )}
            {isActive && (
              <div style={{position:"absolute",top:12,right:plan.id==="gold"?90:12,
                padding:"3px 9px",borderRadius:999,
                background:"rgba(74,222,128,0.12)",border:"1px solid rgba(74,222,128,0.3)",
                fontSize:9,fontWeight:800,color:"#4ADE80",display:"flex",alignItems:"center",gap:4}}>
                <div style={{width:4,height:4,borderRadius:"50%",background:"#4ADE80",
                  boxShadow:"0 0 4px #4ADE80",animation:"blink 2s infinite"}}/>
                ACTIVE
              </div>
            )}

            <div style={{padding:"16px 16px 0"}}>
              <div style={{display:"flex",alignItems:"center",gap:10,marginBottom:12}}>
                <div style={{fontSize:26}}>{plan.icon}</div>
                <div>
                  <div style={{fontSize:15,fontWeight:800,color:plan.clr,letterSpacing:"-.3px"}}>{plan.name} Plan</div>
                  <div style={{fontSize:10,color:"#6B7BA4",marginTop:1}}>
                    ${plan.min.toLocaleString()}{plan.max ? ` – $${plan.max.toLocaleString()}` : "+"}
                  </div>
                </div>
                <div style={{marginLeft:"auto",textAlign:"right"}}>
                  <div style={{fontSize:24,fontWeight:900,color:plan.clr,letterSpacing:"-1px",lineHeight:1}}>{plan.daily}%</div>
                  <div style={{fontSize:8,color:"#546190",fontWeight:700,letterSpacing:.5}}>DAILY</div>
                </div>
              </div>

              <div style={{display:"flex",flexDirection:"column",gap:7,marginBottom:14}}>
                {plan.features.map((f,i) => (
                  <div key={i} style={{display:"flex",alignItems:"center",gap:9}}>
                    <div style={{width:15,height:15,borderRadius:"50%",flexShrink:0,
                      background:`${plan.clr}15`,border:`1px solid ${plan.clr}28`,
                      display:"flex",alignItems:"center",justifyContent:"center"}}>
                      <Check size={8} color={plan.clr} strokeWidth={3}/>
                    </div>
                    <span style={{fontSize:11,color:"#AAB8D4"}}>{f}</span>
                  </div>
                ))}
              </div>

              <div style={{display:"flex",justifyContent:"space-between",alignItems:"center",
                padding:"8px 10px",borderRadius:8,
                background:"rgba(120,140,200,0.05)",border:"1px solid rgba(120,140,200,0.09)",
                marginBottom:12}}>
                <span style={{fontSize:10,color:"#546190"}}>Min. Deposit</span>
                <span style={{fontSize:12,fontWeight:700,color:"#E8EAF6"}}>${plan.min.toLocaleString()}</span>
              </div>
            </div>

            <div style={{padding:"0 16px 16px"}}>
              <button onClick={() => { onSelectPlan(plan); go("deposit"); }} style={{
                width:"100%",padding:"12px",borderRadius:10,border:"none",cursor:"pointer",
                background:`linear-gradient(135deg,${plan.clr},${plan.clr}BB)`,
                color:"#000",fontWeight:800,fontSize:13,
                display:"flex",alignItems:"center",justifyContent:"center",gap:8,
                boxShadow:`0 4px 16px ${plan.clr}30`,
                transition:"all .2s",
              }}
                onMouseEnter={e=>{e.currentTarget.style.transform="scale(1.01)";e.currentTarget.style.boxShadow=`0 6px 22px ${plan.clr}50`;}}
                onMouseLeave={e=>{e.currentTarget.style.transform="scale(1)";e.currentTarget.style.boxShadow=`0 4px 16px ${plan.clr}30`;}}
              >
                {isActive ? "Deposit Again" : "Get Started"} <ArrowRight size={13}/>
              </button>
            </div>
          </div>
        );
      })}

      <div style={{padding:"11px 14px",borderRadius:10,
        background:"rgba(120,140,200,0.03)",border:"1px solid rgba(120,140,200,0.08)",
        display:"flex",alignItems:"flex-start",gap:10}}>
        <Shield size={12} color="#546190" style={{flexShrink:0,marginTop:1}}/>
        <span style={{fontSize:10,color:"#3D4F7C",lineHeight:1.7}}>
          All plans include 10% referral bonus, compounding interest, and multi-sig cold storage protection.
        </span>
      </div>

      <style>{`
        @keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}
        @keyframes blink{0%,100%{opacity:1}50%{opacity:.25}}
      `}</style>
    </div>
  );
}


/* ═══ PROFILE ═══ */
function Profile() {
  const fields = [
    {l:"Account Level",  v:"Standard"},
    {l:"2FA Status",     v:"Disabled"},
    {l:"API Access",     v:"Disabled"},
    {l:"Member Since",   v:"2026"},
  ];
  return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:12,boxSizing:"border-box"}}>
      {/* KYC banner */}
      <Card style={{padding:"14px 16px",
        background:"linear-gradient(120deg,rgba(251,146,60,.08) 0%,rgba(13,13,20,0) 70%)",
        border:"1px solid rgba(251,146,60,.25)",
        display:"flex",alignItems:"flex-start",gap:12,position:"relative",overflow:"hidden"}}>
        <div style={{position:"absolute",top:-30,right:-30,width:120,height:120,borderRadius:"50%",
          background:"radial-gradient(circle,rgba(251,146,60,0.12),transparent 70%)",pointerEvents:"none"}}/>
        <Shield size={18} color="#FB923C" style={{flexShrink:0,marginTop:1}}/>
        <div style={{flex:1,minWidth:0}}>
          <div style={{fontSize:13,fontWeight:700,color:"#FB923C",marginBottom:3}}>Complete Verification (KYC)</div>
          <div style={{fontSize:12,color:"#7C4A1E",lineHeight:1.6,marginBottom:10}}>
            Verify your identity to unlock higher limits and full platform access.
          </div>
          <button style={{padding:"7px 14px",borderRadius:8,background:"rgba(251,146,60,.14)",
            border:"1px solid rgba(251,146,60,.3)",color:"#FB923C",fontSize:12,fontWeight:700,cursor:"pointer"}}>
            Verify Now →
          </button>
        </div>
      </Card>

      {/* account card */}
      <Card style={{padding:"20px",textAlign:"center",position:"relative",overflow:"hidden",
        background:"linear-gradient(160deg,rgba(0,232,122,0.05) 0%,#0D0D14 50%)"}}>
        <div style={{position:"absolute",top:-40,left:"50%",transform:"translateX(-50%)",
          width:200,height:200,borderRadius:"50%",
          background:`radial-gradient(circle,${G}12,transparent 70%)`,pointerEvents:"none"}}/>
        <div style={{
          width:60,height:60,borderRadius:16,
          background:`${G}14`,border:`1px solid ${G}30`,
          boxShadow:`0 0 20px ${G}20`,
          display:"flex",alignItems:"center",justifyContent:"center",
          margin:"0 auto 12px",position:"relative",zIndex:1,
        }}>
          <User size={26} color={G}/>
        </div>
        <div style={{fontSize:14,fontWeight:700,color:"#E8EAF6",marginBottom:6,position:"relative",zIndex:1}}>
          My Account
        </div>
        <div style={{display:"inline-flex",alignItems:"center",gap:5,padding:"3px 10px",borderRadius:999,
          background:"rgba(251,146,60,.1)",border:"1px solid rgba(251,146,60,.22)",position:"relative",zIndex:1}}>
          <div style={{width:5,height:5,borderRadius:"50%",background:"#FB923C"}}/>
          <span style={{fontSize:10,color:"#FB923C",fontWeight:700}}>Unverified</span>
        </div>
        <div style={{marginTop:16,display:"flex",flexDirection:"column",gap:8,position:"relative",zIndex:1}}>
          {[{l:"Plan",v:"Standard"},{l:"Status",v:"Active"}].map(({l,v})=>(
            <div key={l} style={{display:"flex",justifyContent:"space-between",padding:"8px 0",borderTop:"1px solid rgba(120,140,200,0.10)"}}>
              <span style={{fontSize:12,color:"#546190"}}>{l}</span>
              <span style={{fontSize:12,fontWeight:600,color:"#7A8DB4"}}>{v}</span>
            </div>
          ))}
        </div>
      </Card>

      {/* account info */}
      <Card style={{padding:"16px",position:"relative",overflow:"hidden"}}>
        <div style={{position:"absolute",bottom:-40,right:-40,width:160,height:160,borderRadius:"50%",
          background:"radial-gradient(circle,rgba(99,120,234,0.08),transparent 70%)",pointerEvents:"none"}}/>
        <h3 style={{margin:"0 0 12px",fontSize:13,fontWeight:700,color:"#E8EAF6"}}>Account Settings</h3>
        <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:8}}>
          {fields.map(({l,v})=>(
            <div key={l} style={{padding:"12px",borderRadius:9,
              background:"rgba(120,140,200,0.05)",border:"1px solid rgba(120,140,200,0.12)"}}>
              <div style={{fontSize:9,color:"#546190",marginBottom:5,letterSpacing:.8,textTransform:"uppercase",fontWeight:700}}>{l}</div>
              <div style={{fontSize:13,fontWeight:600,color:"#E8EAF6"}}>{v}</div>
            </div>
          ))}
        </div>
      </Card>
    </div>
  );
}

/* ═══ SUPPORT ═══ */
function Support() {
  const { dark, T } = useTheme();
  const [view, setView]       = useState("home"); // "home" | "chat" | "faq"
  const [messages, setMessages] = useState([
    { role:"assistant", text:"👋 Hi! I'm **Aether AI**, your AetherLink Capital support assistant.\n\nI can help you with deposits, withdrawals, investment plans, profits, and account questions. How can I help you today?", ts: Date.now() }
  ]);
  const [input, setInput]     = useState("");
  const [typing, setTyping]   = useState(false);
  const [open, setOpen]       = useState(null);
  const bottomRef             = useRef(null);
  const inputRef              = useRef(null);

  const faqs = [
    {q:"How long do deposits take?",       a:"Deposits are credited after 1–3 network confirmations — typically 10–60 minutes depending on network congestion."},
    {q:"What is the minimum deposit?",     a:"Minimum deposits vary by plan: Bronze starts at $200, Silver at $5,000, Gold at $20,000, and Platinum at $50,000."},
    {q:"What is the minimum withdrawal?",  a:"The minimum withdrawal is $10 USD equivalent. Only live profits are withdrawable — your principal remains active in your plan."},
    {q:"How do withdrawals work?",         a:"Submit a withdrawal request with your wallet address. Our team reviews within 24–48 hours then broadcasts to the network."},
    {q:"How is my daily profit calculated?",a:"Profit = Deposited Amount × Daily Rate ÷ 100. It accrues every second from the moment your deposit is confirmed."},
    {q:"Is my crypto secure?",             a:"Yes. We use multi-signature cold storage, 2FA enforcement, and real-time fraud monitoring on all accounts."},
    {q:"How do I get KYC verified?",       a:"Go to Profile and tap 'Verify Now'. Submit a government-issued ID and a live selfie. Verification typically takes 24 hours."},
    {q:"Can I have multiple active plans?", a:"Yes — you can deposit into multiple plans simultaneously. Each deposit tracks its own profit independently."},
  ];

  useEffect(() => {
    bottomRef.current?.scrollIntoView({ behavior:"smooth" });
  }, [messages, typing]);

  const sendMessage = async () => {
    const text = input.trim();
    if (!text || typing) return;
    setInput("");
    const userMsg = { role:"user", text, ts: Date.now() };
    setMessages(prev => [...prev, userMsg]);
    setTyping(true);

    try {
      const res = await fetch("https://api.anthropic.com/v1/messages", {
        method:"POST",
        headers:{ "content-type":"application/json", "anthropic-version":"2023-06-01" },
        body: JSON.stringify({
          model: "claude-sonnet-4-20250514",
          max_tokens: 600,
          system: `You are Aether AI, the friendly and professional support assistant for AetherLink Capital — a premium crypto investment platform.

Platform details:
- Investment Plans: Bronze ($200–$4,999 · 3%/day), Silver ($5K–$19,999 · 5.5%/day), Gold ($20K–$49,999 · 8%/day), Platinum ($50K+ · 12%/day)
- All plans include 10% referral bonus and daily compounding
- Supported coins: BTC, ETH, USDT (ERC-20 and BEP-20)
- BTC address: bc1qtjzjauzdfd349xl3xzfn7z3a4a6k3tsmc98m66
- ETH/USDT address: 0x18d783350a128CABB231A8Cf30659A2c6DFCdF76
- Withdrawals: only profits are withdrawable, minimum $10 USD, processed within 24–48 hours
- KYC: required for full access, submit via Profile page
- Support email: support@aetherlinkcapital.com

Tone: Warm, professional, concise. Use short paragraphs. Use **bold** for key terms. Never give financial advice. If asked about something outside your knowledge, direct them to support@aetherlinkcapital.com. Keep answers under 120 words.`,
          messages: [
            ...messages.filter(m=>m.role!=="system").map(m=>({
              role: m.role === "assistant" ? "assistant" : "user",
              content: m.text.replace(/\*\*/g,"")
            })),
            { role:"user", content: text }
          ]
        })
      });
      const data = await res.json();
      const reply = data.content?.[0]?.text || "I'm having trouble responding right now. Please try again or email support@aetherlinkcapital.com.";
      setMessages(prev => [...prev, { role:"assistant", text: reply, ts: Date.now() }]);
    } catch {
      setMessages(prev => [...prev, {
        role:"assistant",
        text:"I'm temporarily offline. Please email **support@aetherlinkcapital.com** and we'll respond within 24 hours.",
        ts: Date.now()
      }]);
    }
    setTyping(false);
    setTimeout(() => inputRef.current?.focus(), 100);
  };

  const quickReplies = [
    "How do I deposit?",
    "What plans are available?",
    "How do I withdraw?",
    "When do I get profit?",
  ];

  const renderText = (text) => {
    const parts = text.split(/(\*\*[^*]+\*\*)/g);
    return parts.map((p,i) =>
      p.startsWith("**") && p.endsWith("**")
        ? <strong key={i} style={{color:T.text,fontWeight:700}}>{p.slice(2,-2)}</strong>
        : <span key={i}>{p}</span>
    );
  };

  /* HOME */
  if (view === "home") return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:12}}>
      {/* Hero */}
      <div style={{borderRadius:16,padding:"22px 18px",
        background:"linear-gradient(135deg,rgba(201,168,76,0.12),rgba(124,111,205,0.06))",
        border:`1px solid rgba(201,168,76,0.22)`,backdropFilter:"blur(20px)",
        position:"relative",overflow:"hidden",textAlign:"center"}}>
        <div style={{position:"absolute",top:0,left:0,right:0,height:1,
          background:"linear-gradient(90deg,transparent,rgba(201,168,76,0.6),transparent)",
          backgroundSize:"200% 100%",animation:"shimmer 2.5s linear infinite"}}/>
        {/* AI avatar */}
        <div style={{width:60,height:60,borderRadius:18,margin:"0 auto 14px",
          background:`linear-gradient(135deg,${G},${GD})`,
          boxShadow:`0 0 24px ${G}40`,
          display:"flex",alignItems:"center",justifyContent:"center",fontSize:28}}>🤖</div>
        <h2 style={{margin:"0 0 6px",fontSize:17,fontWeight:800,color:T.text,letterSpacing:"-.3px"}}>
          Aether AI Support
        </h2>
        <p style={{margin:"0 0 18px",fontSize:12,color:T.textSub,lineHeight:1.7}}>
          Instant answers powered by AI. Available 24/7.
        </p>
        <button onClick={()=>setView("chat")} style={{
          display:"inline-flex",alignItems:"center",gap:8,
          padding:"11px 28px",borderRadius:11,border:"none",cursor:"pointer",
          background:`linear-gradient(135deg,${G},${GD})`,
          color:"#000",fontWeight:800,fontSize:13,
          boxShadow:`0 4px 20px ${G}35`,
        }}>
          💬 Chat with Aether AI
        </button>
      </div>

      {/* Quick options */}
      <div style={{display:"grid",gridTemplateColumns:"1fr 1fr",gap:10}}>
        {[
          {icon:"💬",label:"AI Chat",     desc:"Instant AI answers",     action:()=>setView("chat"), clr:G},
          {icon:"❓",label:"FAQ",         desc:"Common questions",        action:()=>setView("faq"),  clr:"#60A5FA"},
          {icon:"📧",label:"Email Us",    desc:"support@aetherlinkcapital.com", action:()=>{}, clr:"#C084FC"},
          {icon:"🔒",label:"Security",    desc:"Report a vulnerability",  action:()=>{}, clr:"#F59E0B"},
        ].map(({icon,label,desc,action,clr})=>(
          <button key={label} onClick={action} style={{
            padding:"14px 12px",borderRadius:12,border:`1px solid ${clr}22`,
            background:dark?`${clr}08`:`${clr}06`,
            cursor:"pointer",textAlign:"left",display:"flex",flexDirection:"column",gap:5,
            transition:"border-color .15s",
          }}
            onMouseEnter={e=>e.currentTarget.style.borderColor=`${clr}40`}
            onMouseLeave={e=>e.currentTarget.style.borderColor=`${clr}22`}
          >
            <div style={{fontSize:20}}>{icon}</div>
            <div style={{fontSize:12,fontWeight:700,color:T.text}}>{label}</div>
            <div style={{fontSize:10,color:T.textSub,lineHeight:1.5}}>{desc}</div>
          </button>
        ))}
      </div>

      {/* Status */}
      <div style={{padding:"12px 14px",borderRadius:11,
        background:dark?"rgba(74,222,128,0.06)":"rgba(74,222,128,0.08)",
        border:"1px solid rgba(74,222,128,0.2)",
        display:"flex",alignItems:"center",gap:10}}>
        <div style={{width:8,height:8,borderRadius:"50%",background:"#4ADE80",
          boxShadow:"0 0 6px #4ADE80",animation:"blink 2s infinite",flexShrink:0}}/>
        <span style={{fontSize:11,color:"#4ADE80",fontWeight:600}}>All systems operational · AI support available 24/7</span>
      </div>
    </div>
  );

  /* FAQ */
  if (view === "faq") return (
    <div style={{padding:"14px",display:"flex",flexDirection:"column",gap:12}}>
      <div style={{display:"flex",alignItems:"center",gap:10,marginBottom:2}}>
        <button onClick={()=>setView("home")} style={{
          width:32,height:32,borderRadius:9,border:`1px solid ${T.borderSub}`,
          background:"transparent",cursor:"pointer",color:T.textSub,
          display:"flex",alignItems:"center",justifyContent:"center",flexShrink:0}}>
          <ChevronRight size={14} style={{transform:"rotate(180deg)"}}/>
        </button>
        <h2 style={{margin:0,fontSize:15,fontWeight:800,color:T.text}}>Frequently Asked Questions</h2>
      </div>
      <div style={{display:"flex",flexDirection:"column",gap:8}}>
        {faqs.map((f,i)=>(
          <div key={i} style={{borderRadius:11,overflow:"hidden",
            background:open===i?`${G}05`:T.card,
            border:`1px solid ${open===i?G+"30":T.borderSub}`,transition:"all .15s"}}>
            <button onClick={()=>setOpen(open===i?null:i)} style={{
              width:"100%",display:"flex",justifyContent:"space-between",alignItems:"center",
              padding:"13px 15px",background:"none",border:"none",cursor:"pointer",
              color:open===i?T.text:T.textSub,fontSize:12,fontWeight:600,textAlign:"left",gap:12}}>
              <span style={{flex:1}}>{f.q}</span>
              <ChevronDown size={13} color={T.textSub}
                style={{transform:open===i?"rotate(180deg)":"rotate(0)",transition:"transform .2s",flexShrink:0}}/>
            </button>
            {open===i&&(
              <div style={{padding:"0 15px 13px",fontSize:12,color:T.textSub,lineHeight:1.8,
                borderTop:`1px solid ${T.borderSub}`}}>{f.a}</div>
            )}
          </div>
        ))}
      </div>
      <button onClick={()=>setView("chat")} style={{
        display:"flex",alignItems:"center",justifyContent:"center",gap:7,
        padding:"11px",borderRadius:10,border:`1px solid ${G}30`,
        background:`${G}10`,color:G,fontSize:12,fontWeight:700,cursor:"pointer"}}>
        💬 Still have questions? Chat with Aether AI
      </button>
    </div>
  );

  /* CHAT */
  return (
    <div style={{display:"flex",flexDirection:"column",height:"calc(100vh - 120px)",padding:"0"}}>

      {/* Chat header */}
      <div style={{padding:"12px 14px",display:"flex",alignItems:"center",gap:10,
        background:T.header,backdropFilter:"blur(20px)",
        borderBottom:`1px solid ${T.border}`,flexShrink:0}}>
        <button onClick={()=>setView("home")} style={{
          width:30,height:30,borderRadius:8,border:`1px solid ${T.borderSub}`,
          background:"transparent",cursor:"pointer",color:T.textSub,
          display:"flex",alignItems:"center",justifyContent:"center",flexShrink:0}}>
          <ChevronRight size={13} style={{transform:"rotate(180deg)"}}/>
        </button>
        <div style={{width:36,height:36,borderRadius:11,flexShrink:0,
          background:`linear-gradient(135deg,${G},${GD})`,
          display:"flex",alignItems:"center",justifyContent:"center",fontSize:18}}>🤖</div>
        <div style={{flex:1,minWidth:0}}>
          <div style={{fontSize:13,fontWeight:700,color:T.text}}>Aether AI</div>
          <div style={{display:"flex",alignItems:"center",gap:5}}>
            <div style={{width:6,height:6,borderRadius:"50%",background:"#4ADE80",
              boxShadow:"0 0 5px #4ADE80",animation:"blink 1.5s infinite"}}/>
            <span style={{fontSize:10,color:"#4ADE80",fontWeight:600}}>Online · Powered by Claude</span>
          </div>
        </div>
        <button onClick={()=>{ setMessages([messages[0]]); }} style={{
          fontSize:10,color:T.textMuted,background:"none",border:"none",cursor:"pointer",fontWeight:600}}>
          Clear
        </button>
      </div>

      {/* Messages */}
      <div style={{flex:1,overflowY:"auto",padding:"14px",display:"flex",flexDirection:"column",gap:10}}>
        {messages.map((m,i)=>(
          <div key={i} style={{display:"flex",gap:8,
            flexDirection:m.role==="user"?"row-reverse":"row",
            alignItems:"flex-end"}}>
            {m.role==="assistant"&&(
              <div style={{width:28,height:28,borderRadius:8,flexShrink:0,
                background:`linear-gradient(135deg,${G},${GD})`,
                display:"flex",alignItems:"center",justifyContent:"center",fontSize:14}}>🤖</div>
            )}
            <div style={{
              maxWidth:"78%",padding:"10px 13px",borderRadius:14,
              borderBottomLeftRadius:m.role==="assistant"?4:14,
              borderBottomRightRadius:m.role==="user"?4:14,
              background: m.role==="user"
                ? `linear-gradient(135deg,${G},${GD})`
                : dark?"rgba(30,25,60,0.90)":"rgba(245,246,255,0.95)",
              border: m.role==="user" ? "none" : `1px solid ${T.borderSub}`,
              fontSize:12,lineHeight:1.7,
              color: m.role==="user" ? "#000" : T.text,
              fontWeight: m.role==="user" ? 600 : 400,
            }}>
              {m.role==="assistant" ? renderText(m.text) : m.text}
              <div style={{fontSize:9,color:m.role==="user"?"rgba(0,0,0,0.5)":T.textMuted,
                marginTop:4,textAlign:m.role==="user"?"right":"left"}}>
                {new Date(m.ts).toLocaleTimeString("en-US",{hour:"2-digit",minute:"2-digit"})}
              </div>
            </div>
          </div>
        ))}

        {/* Typing indicator */}
        {typing&&(
          <div style={{display:"flex",gap:8,alignItems:"flex-end"}}>
            <div style={{width:28,height:28,borderRadius:8,flexShrink:0,
              background:`linear-gradient(135deg,${G},${GD})`,
              display:"flex",alignItems:"center",justifyContent:"center",fontSize:14}}>🤖</div>
            <div style={{padding:"12px 16px",borderRadius:14,borderBottomLeftRadius:4,
              background:dark?"rgba(30,25,60,0.90)":"rgba(245,246,255,0.95)",
              border:`1px solid ${T.borderSub}`,
              display:"flex",alignItems:"center",gap:4}}>
              {[0,1,2].map(i=>(
                <div key={i} style={{width:7,height:7,borderRadius:"50%",background:G,
                  animation:`blink 1.2s ease-in-out ${i*0.2}s infinite`}}/>
              ))}
            </div>
          </div>
        )}

        {/* Quick replies — show only after first message */}
        {messages.length===1&&!typing&&(
          <div style={{display:"flex",flexWrap:"wrap",gap:7,marginTop:4}}>
            {quickReplies.map(q=>(
              <button key={q} onClick={()=>{setInput(q);setTimeout(()=>{ setInput(""); const userMsg={role:"user",text:q,ts:Date.now()}; setMessages(prev=>[...prev,userMsg]); setTyping(true);
                fetch("https://api.anthropic.com/v1/messages",{method:"POST",headers:{"content-type":"application/json","anthropic-version":"2023-06-01"},body:JSON.stringify({model:"claude-sonnet-4-20250514",max_tokens:400,system:"You are Aether AI, support assistant for AetherLink Capital — a crypto investment platform. Plans: Bronze $200+ 3%/day, Silver $5K+ 5.5%/day, Gold $20K+ 8%/day, Platinum $50K+ 12%/day. Withdrawals processed in 24-48h. Deposits via BTC/ETH/USDT. Be concise, warm, professional. Under 80 words.",messages:[{role:"user",content:q}]})}).then(r=>r.json()).then(d=>{setMessages(prev=>[...prev,{role:"assistant",text:d.content?.[0]?.text||"Let me check that for you. Email support@aetherlinkcapital.com if this persists.",ts:Date.now()}]);setTyping(false);}).catch(()=>{setMessages(prev=>[...prev,{role:"assistant",text:"Sorry, I'm offline. Email support@aetherlinkcapital.com.",ts:Date.now()}]);setTyping(false);}); },50);}} style={{
                padding:"7px 12px",borderRadius:20,
                background:dark?`${G}10`:"rgba(201,168,76,0.10)",
                border:`1px solid ${G}25`,
                color:G,fontSize:11,fontWeight:600,cursor:"pointer",
                transition:"all .15s",
              }}>
                {q}
              </button>
            ))}
          </div>
        )}
        <div ref={bottomRef}/>
      </div>

      {/* Input bar */}
      <div style={{padding:"10px 14px",
        background:T.header,backdropFilter:"blur(20px)",
        borderTop:`1px solid ${T.border}`,flexShrink:0,
        display:"flex",gap:9,alignItems:"flex-end"}}>
        <input
          ref={inputRef}
          value={input}
          onChange={e=>setInput(e.target.value)}
          onKeyDown={e=>e.key==="Enter"&&!e.shiftKey&&sendMessage()}
          placeholder="Ask anything about AetherLink…"
          style={{
            flex:1,padding:"10px 14px",borderRadius:22,
            background:dark?"rgba(30,25,60,0.80)":"rgba(240,242,255,0.95)",
            border:`1px solid ${T.borderSub}`,
            color:T.text,fontSize:13,outline:"none",
            fontFamily:"inherit",resize:"none",
            transition:"border-color .18s",
          }}
          onFocus={e=>e.target.style.borderColor=`${G}50`}
          onBlur={e=>e.target.style.borderColor=T.borderSub}
        />
        <button onClick={sendMessage} disabled={!input.trim()||typing} style={{
          width:40,height:40,borderRadius:"50%",border:"none",flexShrink:0,cursor:"pointer",
          background:input.trim()&&!typing
            ? `linear-gradient(135deg,${G},${GD})`
            : "rgba(120,140,200,0.15)",
          display:"flex",alignItems:"center",justifyContent:"center",
          transition:"all .2s",
          boxShadow:input.trim()&&!typing?`0 0 14px ${G}40`:"none",
        }}>
          <ArrowRight size={16} color={input.trim()&&!typing?"#000":"#546190"}/>
        </button>
      </div>
    </div>
  );
}

/* ═══ ROOT ═══ */
export default function App() {
  const [screen, setScreen]   = useState("dashboard");
  const [sideOpen, setSideOpen] = useState(false);

  // ── Theme: detect system, persist choice ──
  const [dark, setDark] = useState(() => {
    try {
      const saved = localStorage.getItem("aetherlink_theme");
      if (saved !== null) return saved === "dark";
    } catch {}
    return window.matchMedia?.("(prefers-color-scheme: dark)").matches ?? true;
  });

  // Listen for system changes if user hasn't manually set it
  useEffect(() => {
    const mq = window.matchMedia?.("(prefers-color-scheme: dark)");
    if (!mq) return;
    const handler = (e) => {
      try {
        if (!localStorage.getItem("aetherlink_theme")) setDark(e.matches);
      } catch { setDark(e.matches); }
    };
    mq.addEventListener("change", handler);
    return () => mq.removeEventListener("change", handler);
  }, []);

  const toggleTheme = () => {
    setDark(d => {
      const next = !d;
      try { localStorage.setItem("aetherlink_theme", next ? "dark" : "light"); } catch {}
      return next;
    });
  };

  const T = dark ? DARK : LIGHT;

  // ── Persisted state — survives browser refresh/close ──
  const [txns, setTxnsRaw] = useState(() => {
    try {
      const saved = localStorage.getItem("aetherlink_txns");
      return saved ? JSON.parse(saved) : [];
    } catch { return []; }
  });

  const [selectedPlan, setSelectedPlanRaw] = useState(() => {
    try {
      const saved = localStorage.getItem("aetherlink_plan");
      return saved ? JSON.parse(saved) : null;
    } catch { return null; }
  });

  // Wrap setters to also persist to localStorage
  const setTxns = (updater) => {
    setTxnsRaw(prev => {
      const next = typeof updater === "function" ? updater(prev) : updater;
      try { localStorage.setItem("aetherlink_txns", JSON.stringify(next)); } catch {}
      return next;
    });
  };

  const setSelectedPlan = (plan) => {
    setSelectedPlanRaw(plan);
    try {
      if (plan) localStorage.setItem("aetherlink_plan", JSON.stringify(plan));
      else localStorage.removeItem("aetherlink_plan");
    } catch {}
  };

  const addTx = (tx) => setTxns(prev => [tx, ...prev]);

  const clearAll = () => {
    setTxns([]);
    setSelectedPlan(null);
    try { localStorage.removeItem("aetherlink_txns"); localStorage.removeItem("aetherlink_plan"); } catch {}
  };

  const { COINS, TICKS, lastUpdate, fetching, connected, refresh } = usePrices();

  // Stable screen props — memoized so component identity never changes on keystroke
  const screenProps = {
    go: setScreen,
    COINS,
    txns,
    selectedPlan,
    onTxSubmit: addTx,
    onClear: clearAll,
    onSelectPlan: setSelectedPlan,
  };


  return (
    <ThemeCtx.Provider value={{ dark, toggle: toggleTheme, T }}>
      <div style={{
        width:"100vw", height:"100vh", display:"flex", flexDirection:"column",
        background: T.bg,
        fontFamily:"'DM Sans','SF Pro Text',-apple-system,sans-serif",
        color: T.text,
        overflow:"hidden", position:"relative",
        transition:"background 0.4s ease, color 0.4s ease",
      }}>
        <style>{`
          @import url('https://fonts.googleapis.com/css2?family=DM+Sans:opsz,wght@9..40,400;9..40,500;9..40,600;9..40,700;9..40,800;9..40,900&display=swap');
          *{box-sizing:border-box;-webkit-font-smoothing:antialiased;margin:0;padding:0;}
          ::-webkit-scrollbar{width:3px;}
          ::-webkit-scrollbar-track{background:transparent;}
          ::-webkit-scrollbar-thumb{background:rgba(201,168,76,0.25);border-radius:99px;}
          input::placeholder{color:${dark?"#2A3558":"#9AA5CC"};}
          input,button{font-family:inherit;}
          @keyframes blink{0%,100%{opacity:1}50%{opacity:.2}}
          @keyframes spin{to{transform:rotate(360deg)}}
          @keyframes float{0%,100%{transform:translateY(0)}50%{transform:translateY(-18px)}}
          @keyframes pulse-glow{0%,100%{opacity:.4}50%{opacity:.9}}
          @keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}
          /* smooth theme transitions on all elements */
          div,span,p,h1,h2,h3,h4,button,input,nav,aside,header,main,footer{
            transition: background-color 0.35s ease, border-color 0.35s ease, color 0.3s ease;
          }
        `}</style>

        {/* Animated canvas — only in dark mode */}
        {dark && <AnimatedBG/>}
        {/* Light mode: subtle gradient background */}
        {!dark && (
          <div style={{position:"fixed",inset:0,zIndex:0,pointerEvents:"none",
            background:"radial-gradient(ellipse at 20% 20%,rgba(201,168,76,0.06) 0%,transparent 60%), radial-gradient(ellipse at 80% 80%,rgba(124,111,205,0.05) 0%,transparent 60%)"}}/>
        )}

        {/* Content layer */}
        <div style={{position:"relative",zIndex:1,display:"flex",flexDirection:"column",height:"100%",overflow:"hidden"}}>

          {/* Ticker bar */}
          <div style={{height:32,
            background: T.ticker,
            borderBottom:`1px solid ${T.border}`,
            backdropFilter:"blur(20px)",
            overflow:"hidden",display:"flex",alignItems:"center",flexShrink:0,width:"100%"}}>
            <div style={{padding:"0 12px",borderRight:`1px solid ${T.border}`,height:"100%",
              display:"flex",alignItems:"center",gap:5,flexShrink:0}}>
              <div style={{width:5,height:5,borderRadius:"50%",background:G,
                boxShadow:`0 0 8px ${G}`,animation:"blink 2s infinite"}}/>
              <span style={{fontSize:9,fontWeight:800,color:G,letterSpacing:1.5,textTransform:"uppercase",whiteSpace:"nowrap"}}>Live</span>
            </div>
            <div style={{overflow:"hidden",flex:1}}>
              <TickerScroll TICKS={TICKS}/>
            </div>
            {lastUpdate && (
              <div style={{display:"flex",alignItems:"center",gap:6,padding:"0 10px",flexShrink:0,
                borderLeft:`1px solid ${T.border}`}}>
                <span style={{fontSize:9,color:T.textSub,whiteSpace:"nowrap"}}>
                  {lastUpdate.toLocaleTimeString("en-US",{hour:"2-digit",minute:"2-digit",second:"2-digit"})}
                </span>
                <button onClick={refresh} style={{background:"none",border:"none",cursor:"pointer",
                  color:fetching?G:T.textSub,padding:0,display:"flex",alignItems:"center"}}>
                  <RefreshCw size={9} style={{animation:fetching?"spin 1s linear infinite":"none"}}/>
                </button>
              </div>
            )}
          </div>

          <div style={{display:"flex",flex:1,minHeight:0}}>
            <Sidebar active={screen} go={setScreen} open={sideOpen} onClose={()=>setSideOpen(false)}/>
            <main style={{flex:1,display:"flex",flexDirection:"column",minWidth:0,overflow:"hidden",width:"100%"}}>
              <Topbar
                screen={screen} onMenu={()=>setSideOpen(true)}
                COINS={COINS} lastUpdate={lastUpdate} fetching={fetching}
                connected={connected} refresh={refresh}
                dark={dark} toggleTheme={toggleTheme}
              />
              <div style={{flex:1,overflowY:"auto",overflowX:"hidden",background:T.bg}}>
                {screen === "dashboard"    && <Dashboard    go={screenProps.go} COINS={screenProps.COINS} txns={screenProps.txns}/>}
                {screen === "plans"        && <Plans        go={screenProps.go} onSelectPlan={screenProps.onSelectPlan} txns={screenProps.txns}/>}
                {screen === "deposit"      && <Deposit      go={screenProps.go} COINS={screenProps.COINS} selectedPlan={screenProps.selectedPlan} onTxSubmit={screenProps.onTxSubmit}/>}
                {screen === "withdraw"     && <Withdraw     COINS={screenProps.COINS} txns={screenProps.txns}/>}
                {screen === "transactions" && <Transactions txns={screenProps.txns} onClear={screenProps.onClear}/>}
              </div>
              <footer style={{padding:"8px 18px",
                borderTop:`1px solid ${T.border}`,
                display:"flex",justifyContent:"space-between",alignItems:"center",
                flexShrink:0,background:T.header,backdropFilter:"blur(20px)",
                flexWrap:"wrap",gap:8}}>
                <div style={{display:"flex",alignItems:"center",gap:8}}>
                  <svg width="20" height="20" viewBox="0 0 38 38" fill="none">
                    <defs>
                      <linearGradient id="lgFoot2" x1="0" y1="0" x2="38" y2="38" gradientUnits="userSpaceOnUse">
                        <stop offset="0%" stopColor="#E8C97A"/>
                        <stop offset="100%" stopColor="#A07830"/>
                      </linearGradient>
                    </defs>
                    <path d="M19 2 L34 10.5 L34 27.5 L19 36 L4 27.5 L4 10.5 Z" fill="rgba(201,168,76,0.10)" stroke="url(#lgFoot2)" strokeWidth="1"/>
                    <path d="M19 9 L27 28 H23.5 L21.8 23.5 H16.2 L14.5 28 H11 Z M17.2 20.5 H20.8 L19 15.5 Z" fill="url(#lgFoot2)"/>
                  </svg>
                  <span style={{fontSize:11,color:T.textMuted}}>© 2026 AetherLink Capital</span>
                </div>
                <div style={{display:"flex",gap:16}}>
                  {["Terms","Privacy","Compliance"].map(l=>(
                    <a key={l} href="#" style={{fontSize:11,color:T.textMuted,textDecoration:"none"}}>{l}</a>
                  ))}
                </div>
              </footer>
            </main>
          </div>

        </div>
      </div>
    </ThemeCtx.Provider>
  );
}
