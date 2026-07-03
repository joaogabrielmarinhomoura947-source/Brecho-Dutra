import React, { useState, useMemo, useEffect, useRef } from "react";
import {
  Search, Heart, ShoppingBag, User, X, Menu, ChevronRight, ChevronLeft,
  Trash2, Filter, Instagram, MapPin, Clock, Copy, Check, Sparkles,
  LayoutDashboard, Package, Users as UsersIcon, TrendingUp, LogOut, Edit2,
  ArrowLeft, Send, Bot, Shirt, Footprints, Gem, ShoppingBag as BagIcon,
  Plus, Star, MessageCircle, ClipboardList, Wand2
} from "lucide-react";
import {
  LineChart, Line, BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip,
  ResponsiveContainer
} from "recharts";

/* ------------------------------------------------------------------ */
/* FONTS + BASE STYLE                                                  */
/* ------------------------------------------------------------------ */
const FontStyle = () => (
  <style>{`
    @import url('https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,300;0,9..144,450;0,9..144,600;0,9..144,700;1,9..144,400;1,9..144,500&family=Inter:wght@400;500;600;700&family=Space+Mono:wght@400;700&display=swap');
    .font-display { font-family: 'Fraunces', serif; }
    .font-body { font-family: 'Inter', sans-serif; }
    .font-mono { font-family: 'Space Mono', monospace; }
    * { -webkit-tap-highlight-color: transparent; }
    ::selection { background: #B08D57; color: #1C2620; }
    @media (prefers-reduced-motion: reduce) {
      *, *::before, *::after { animation-duration: 0.001ms !important; transition-duration: 0.001ms !important; }
    }
    .tag-hole { box-shadow: inset 0 0 0 2px #1C262022; }
    .scrollbar-thin::-webkit-scrollbar { width: 6px; height: 6px; }
    .scrollbar-thin::-webkit-scrollbar-thumb { background: #B08D5766; border-radius: 4px; }

    /* paper grain, used as a soft overlay across the whole site */
    .grain { position: relative; }
    .grain::before {
      content: ""; position: absolute; inset: 0; pointer-events: none; z-index: 1;
      opacity: 0.05; mix-blend-mode: multiply;
      background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='140' height='140'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='2' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
    }
    .card-lift { transition: transform .45s cubic-bezier(.16,1,.3,1), box-shadow .45s cubic-bezier(.16,1,.3,1); }
    .card-lift:hover { transform: translateY(-4px); box-shadow: 0 18px 30px -18px rgba(28,38,32,0.35); }
    .btn-lift { transition: transform .25s ease, box-shadow .25s ease, background-color .25s ease; }
    .btn-lift:hover { transform: translateY(-2px); }
    .btn-lift:active { transform: translateY(0px) scale(0.98); }
    .stitch { background-image: repeating-linear-gradient(90deg, currentColor 0 6px, transparent 6px 12px); height: 1px; opacity: 0.35; }
    .fade-up { animation: fadeUp .7s cubic-bezier(.16,1,.3,1) both; }
    @keyframes fadeUp { from { opacity: 0; transform: translateY(14px); } to { opacity: 1; transform: translateY(0); } }
    .hover-underline { position: relative; }
    .hover-underline::after {
      content: ""; position: absolute; left: 0; bottom: -2px; height: 1px; width: 0; background: currentColor;
      transition: width .35s cubic-bezier(.16,1,.3,1);
    }
    .hover-underline:hover::after { width: 100%; }
  `}</style>
);

/* ------------------------------------------------------------------ */
/* PALETTE                                                             */
/* ------------------------------------------------------------------ */
const C = {
  ink: "#1C2620",
  forest: "#2F4034",
  parchment: "#EFE7D8",
  parchment2: "#E5DAC4",
  brass: "#B08D57",
  burgundy: "#7A2E2E",
  cream: "#F6F1E7",
};

const CONDITIONS = ["Novo", "Como Novo", "Seminovo", "Usado"];
const CATEGORIES = ["Vestidos", "Blusas", "Calças", "Jaquetas", "Saias", "Bolsas", "Calçados", "Acessórios"];
const GENDERS = ["Feminino", "Masculino", "Unissex"];
const BRANDS = ["Alma Vintage", "Studio Lima", "Nordika", "Verão & Co.", "Casa Bruma", "Retrô Bela", "Traço Fino"];
const COLOR_MAP = {
  "Verde": "#3F5A44", "Preto": "#232323", "Bege": "#C9B89C", "Azul": "#3A5A78",
  "Vinho": "#6B2737", "Branco": "#E9E6DF", "Marrom": "#5B4636", "Terracota": "#A85C3B",
  "Amarelo": "#C9A227", "Rosa": "#B98A94"
};

const iconFor = (cat) => {
  if (cat === "Calçados") return Footprints;
  if (cat === "Bolsas") return BagIcon;
  if (cat === "Acessórios") return Gem;
  return Shirt;
};

/* ------------------------------------------------------------------ */
/* MOCK PRODUCT DATA                                                    */
/* ------------------------------------------------------------------ */
const seedProducts = [
  { id: "p1", name: "Vestido Midi Alfaiataria", brand: "Alma Vintage", category: "Vestidos", color: "Verde", size: "M", gender: "Feminino", condition: "Como Novo", price: 189, description: "Vestido midi em tecido de alfaiataria, corte reto com cinto na cintura. Peça garimpada em ótimo estado, poucas marcas de uso.", featured: true, createdAt: "2026-06-28", sold: 3 },
  { id: "p2", name: "Blazer Xadrez Estruturado", brand: "Studio Lima", category: "Jaquetas", color: "Marrom", size: "G", gender: "Unissex", condition: "Seminovo", price: 165, description: "Blazer de lã xadrez, ombreira estruturada, forro completo. Um clássico atemporal para compor looks de trabalho ou casual chic.", featured: true, createdAt: "2026-06-30", sold: 7 },
  { id: "p3", name: "Camisa Seda Estampada", brand: "Retrô Bela", category: "Blusas", color: "Terracota", size: "P", gender: "Feminino", condition: "Novo", price: 129, description: "Camisa 100% seda com estampa exclusiva, botões de madrepérola. Nunca usada, com etiqueta original.", featured: true, createdAt: "2026-06-25", sold: 12 },
  { id: "p4", name: "Calça Wide Leg Alfaiataria", brand: "Nordika", category: "Calças", color: "Bege", size: "38", gender: "Feminino", condition: "Como Novo", price: 149, description: "Calça de alfaiataria modelagem wide leg, cintura alta com pences. Caimento impecável.", featured: false, createdAt: "2026-06-29", sold: 2 },
  { id: "p5", name: "Jaqueta Jeans Clássica", brand: "Verão & Co.", category: "Jaquetas", color: "Azul", size: "M", gender: "Unissex", condition: "Usado", price: 99, description: "Jaqueta jeans tradicional, lavagem média, leve desbotado que dá charme vintage à peça.", featured: false, createdAt: "2026-06-18", sold: 21 },
  { id: "p6", name: "Saia Midi Plissada", brand: "Casa Bruma", category: "Saias", color: "Vinho", size: "P", gender: "Feminino", condition: "Como Novo", price: 119, description: "Saia midi plissada em tecido fluido, cós elástico. Muito versátil, veste bem em diferentes ocasiões.", featured: false, createdAt: "2026-06-27", sold: 5 },
  { id: "p7", name: "Bolsa Couro Estruturada", brand: "Traço Fino", category: "Bolsas", color: "Marrom", size: "Único", gender: "Unissex", condition: "Seminovo", price: 219, description: "Bolsa em couro legítimo, alça de mão e tiracolo removível. Interior forrado com bolso zíper.", featured: true, createdAt: "2026-06-20", sold: 4 },
  { id: "p8", name: "Bota Coturno Vintage", brand: "Nordika", category: "Calçados", color: "Preto", size: "39", gender: "Unissex", condition: "Seminovo", price: 175, description: "Coturno de couro, solado tratorado. Marcas leves de uso que reforçam o estilo autêntico da peça.", featured: false, createdAt: "2026-06-15", sold: 9 },
  { id: "p9", name: "Colar Contas de Vidro", brand: "Alma Vintage", category: "Acessórios", color: "Amarelo", size: "Único", gender: "Feminino", condition: "Novo", price: 59, description: "Colar artesanal com contas de vidro soprado, fecho em metal dourado envelhecido.", featured: false, createdAt: "2026-07-01", sold: 1 },
  { id: "p10", name: "Cardigã Tricô Trançado", brand: "Casa Bruma", category: "Blusas", color: "Bege", size: "G", gender: "Unissex", condition: "Como Novo", price: 139, description: "Cardigã de tricô com trançado artesanal, botões de madeira. Aconchegante e atemporal.", featured: false, createdAt: "2026-06-22", sold: 6 },
  { id: "p11", name: "Vestido Slip Cetim", brand: "Retrô Bela", category: "Vestidos", color: "Rosa", size: "P", gender: "Feminino", condition: "Novo", price: 159, description: "Vestido slip em cetim com caimento fluido, alças ajustáveis. Peça nunca usada, etiqueta original.", featured: false, createdAt: "2026-07-01", sold: 0 },
  { id: "p12", name: "Calça Cargo Utilitária", brand: "Studio Lima", category: "Calças", color: "Verde", size: "40", gender: "Masculino", condition: "Usado", price: 89, description: "Calça cargo com bolsos laterais, tecido resistente. Uso moderado, sem manchas ou rasgos.", featured: false, createdAt: "2026-06-10", sold: 14 },
  { id: "p13", name: "Óculos de Sol Redondo", brand: "Traço Fino", category: "Acessórios", color: "Preto", size: "Único", gender: "Unissex", condition: "Como Novo", price: 79, description: "Óculos de sol armação redonda em acetato, lentes com proteção UV400.", featured: false, createdAt: "2026-06-30", sold: 3 },
  { id: "p14", name: "Sandália Couro Tiras", brand: "Nordika", category: "Calçados", color: "Marrom", size: "37", gender: "Feminino", condition: "Seminovo", price: 99, description: "Sandália de couro com tiras finas, salto bloco baixo. Confortável para o dia a dia.", featured: false, createdAt: "2026-06-24", sold: 8 },
];

const brl = (v) => v.toLocaleString("pt-BR", { style: "currency", currency: "BRL" });

/* ------------------------------------------------------------------ */
/* PLACEHOLDER "PHOTO" — tinted panel with garment icon                */
/* ------------------------------------------------------------------ */
function PhotoPanel({ product, variant = 0, className = "" }) {
  const Icon = iconFor(product.category);
  const hex = COLOR_MAP[product.color] || "#8A7B63";
  const rot = (variant % 5) * 2.6 - 5.2;
  const photo = product.images && product.images[variant % Math.max(product.images.length, 1)];

  if (photo) {
    return (
      <div className={`relative overflow-hidden flex items-center justify-center ${className}`} style={{ background: C.ink }}>
        <img src={photo} alt={product.name} className="w-full h-full object-cover" />
      </div>
    );
  }

  return (
    <div
      className={`relative overflow-hidden flex items-center justify-center grain ${className}`}
      style={{
        background: `radial-gradient(120% 90% at 30% 15%, ${hex}f2 0%, ${hex}b8 42%, ${C.ink}e6 100%)`,
      }}
    >
      {/* soft diagonal sheen */}
      <div
        className="absolute inset-0 opacity-[0.14]"
        style={{ background: `linear-gradient(115deg, transparent 30%, #ffffff 46%, transparent 62%)` }}
      />
      {/* fine woven texture */}
      <div
        className="absolute inset-0 opacity-[0.08]"
        style={{
          backgroundImage:
            "repeating-linear-gradient(0deg, #ffffff 0px, #ffffff 1px, transparent 1px, transparent 5px), repeating-linear-gradient(90deg, #00000022 0px, #00000022 1px, transparent 1px, transparent 5px)",
        }}
      />
      {/* vignette */}
      <div className="absolute inset-0" style={{ boxShadow: `inset 0 0 46px 6px ${C.ink}55` }} />
      <Icon
        strokeWidth={0.9}
        className="drop-shadow-sm"
        style={{ width: "36%", height: "36%", color: C.cream, opacity: 0.92, transform: `rotate(${rot}deg)` }}
      />
      <span
        className="absolute bottom-2.5 right-3 font-mono text-[9px] tracking-[0.14em] uppercase px-1.5 py-0.5 rounded-sm"
        style={{ color: C.cream, background: `${C.ink}55`, backdropFilter: "blur(2px)" }}
      >
        sem foto · {product.color}
      </span>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* SIGNATURE — hanging price tag                                       */
/* ------------------------------------------------------------------ */
function PriceTag({ price, condition, small }) {
  return (
    <div className="relative inline-flex items-center" style={{ transform: "rotate(-2deg)" }}>
      <div
        className={`relative flex items-center gap-2 font-mono ${small ? "text-[11.5px] pl-2.5 pr-3 py-1" : "text-sm pl-3.5 pr-4 py-1.5"}`}
        style={{
          background: C.parchment,
          border: "1px solid #1C262030",
          borderLeft: `2px solid ${C.brass}`,
          color: C.ink,
          boxShadow: "0 3px 8px -3px rgba(28,38,32,0.28)",
          clipPath: "polygon(0 0, 100% 0, 100% 100%, 0 100%)",
        }}
      >
        <span
          className="rounded-full tag-hole"
          style={{ width: small ? 5 : 7, height: small ? 5 : 7, background: `${C.ink}14`, borderColor: "#1C262055" }}
        />
        <span className="font-bold tracking-tight">{brl(price)}</span>
      </div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* PRODUCT CARD                                                        */
/* ------------------------------------------------------------------ */
function ProductCard({ product, onOpen, onAddCart, isFav, onToggleFav, index }) {
  return (
    <div className="group flex flex-col card-lift rounded-md">
      <div className="relative aspect-[4/5] mb-3.5 overflow-hidden rounded-md shadow-sm">
        <PhotoPanel product={product} variant={index} className="w-full h-full transition-transform duration-700 ease-out group-hover:scale-[1.06]" />
        <div className="absolute inset-0 bg-gradient-to-t from-black/35 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300" />
        <button
          onClick={() => onToggleFav(product.id)}
          aria-label="Favoritar"
          className="absolute top-2.5 right-2.5 w-8 h-8 rounded-full flex items-center justify-center backdrop-blur-sm transition-all hover:scale-110"
          style={{ background: isFav ? C.burgundy : "#1C262055" }}
        >
          <Heart size={14} strokeWidth={2} fill={isFav ? C.cream : "none"} color={C.cream} />
        </button>
        <span
          className="absolute top-2.5 left-2.5 px-2 py-1 text-[9.5px] font-mono tracking-[0.08em] uppercase rounded-sm"
          style={{ background: `${C.cream}e8`, color: C.ink }}
        >
          {product.condition}
        </span>
        <div className="absolute inset-x-0 bottom-0 p-2.5 flex justify-between items-end opacity-0 group-hover:opacity-100 translate-y-2 group-hover:translate-y-0 transition-all duration-300">
          <button
            onClick={() => onOpen(product.id)}
            className="text-[11px] font-body font-medium px-3 py-1.5 rounded-full shadow-sm"
            style={{ background: C.cream, color: C.ink }}
          >
            Ver detalhes
          </button>
          <button
            onClick={() => onAddCart(product.id)}
            className="w-8 h-8 rounded-full flex items-center justify-center shadow-sm btn-lift"
            style={{ background: C.brass, color: C.ink }}
            aria-label="Adicionar ao carrinho"
          >
            <ShoppingBag size={13} />
          </button>
        </div>
      </div>
      <div className="flex items-start justify-between gap-2 px-0.5">
        <div className="min-w-0">
          <p className="font-mono text-[9.5px] tracking-[0.12em] uppercase truncate" style={{ color: C.brass }}>{product.brand}</p>
          <button onClick={() => onOpen(product.id)} className="font-display text-[16px] leading-snug text-left block hover-underline" style={{ color: C.ink }}>
            {product.name}
          </button>
          <p className="font-body text-[11px] mt-0.5" style={{ color: "#847A67" }}>{product.color} · Tam. {product.size}</p>
        </div>
      </div>
      <div className="mt-2 px-0.5"><PriceTag price={product.price} small /></div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* HEADER                                                              */
/* ------------------------------------------------------------------ */
function Header({ nav, route, search, setSearch, cartCount, favCount, user, onCartOpen, onAuthOpen, onAccount, suggestions, onPickSuggestion }) {
  const [menuOpen, setMenuOpen] = useState(false);
  const [searchFocus, setSearchFocus] = useState(false);
  return (
    <header className="sticky top-0 z-40 border-b" style={{ background: C.ink, borderColor: "#ffffff14" }}>
      <div className="max-w-7xl mx-auto px-4 md:px-6">
        <div className="flex items-center justify-between h-16 gap-3">
          <div className="flex items-center gap-2 md:gap-7">
            <button className="md:hidden" onClick={() => setMenuOpen(!menuOpen)} aria-label="Menu">
              {menuOpen ? <X color={C.cream} size={22} /> : <Menu color={C.cream} size={22} />}
            </button>
            <button onClick={() => nav("home")} className="flex items-center gap-2">
              <span
                className="w-8 h-8 rounded-full flex items-center justify-center shrink-0 font-display text-[15px]"
                style={{ background: C.brass, color: C.ink, border: `1px solid ${C.cream}22` }}
              >
                D
              </span>
              <span className="font-display text-[19px] tracking-wide leading-none" style={{ color: C.cream }}>
                Brechó <span className="italic" style={{ color: C.brass }}>Dutra</span>
              </span>
            </button>
            <nav className="hidden md:flex items-center gap-6 font-body text-[13px]">
              {["home", "catalog"].map((r) => (
                <button
                  key={r}
                  onClick={() => nav(r)}
                  className="pb-1 border-b transition-colors"
                  style={{
                    color: route === r ? C.brass : `${C.cream}b8`,
                    borderColor: route === r ? C.brass : "transparent",
                  }}
                >
                  {r === "home" ? "Início" : "Catálogo"}
                </button>
              ))}
            </nav>
          </div>

          <div className="hidden sm:block flex-1 max-w-sm relative">
            <div className="relative">
              <Search size={15} className="absolute left-3.5 top-1/2 -translate-y-1/2" color={`${C.cream}80`} />
              <input
                value={search}
                onChange={(e) => setSearch(e.target.value)}
                onFocus={() => setSearchFocus(true)}
                onBlur={() => setTimeout(() => setSearchFocus(false), 150)}
                placeholder="Buscar por nome, marca, cor..."
                className="w-full font-body text-[13px] pl-9 pr-3 py-2.5 rounded-full outline-none border transition-colors focus:border-[#B08D5788]"
                style={{ background: "#ffffff0d", color: C.cream, borderColor: "#ffffff1a" }}
              />
            </div>
            {searchFocus && search.trim() && (
              <div className="absolute mt-1.5 w-full rounded-md overflow-hidden shadow-xl z-50" style={{ background: C.cream }}>
                {suggestions.length === 0 && (
                  <p className="px-4 py-3 font-body text-[13px]" style={{ color: "#5B5346" }}>Nenhum resultado para "{search}"</p>
                )}
                {suggestions.slice(0, 5).map((p) => (
                  <button
                    key={p.id}
                    onClick={() => onPickSuggestion(p.id)}
                    className="w-full flex items-center gap-3 px-3 py-2 text-left hover:bg-black/5"
                  >
                    <div className="w-9 h-9 rounded-sm overflow-hidden shrink-0"><PhotoPanel product={p} className="w-full h-full" /></div>
                    <div className="min-w-0">
                      <p className="font-body text-[13px] truncate" style={{ color: C.ink }}>{p.name}</p>
                      <p className="font-mono text-[10px]" style={{ color: C.brass }}>{p.brand} · {brl(p.price)}</p>
                    </div>
                  </button>
                ))}
                {suggestions.length > 5 && (
                  <button onClick={() => onPickSuggestion(null)} className="w-full text-center py-2 font-body text-[12px]" style={{ color: C.burgundy }}>
                    Ver todos os {suggestions.length} resultados
                  </button>
                )}
              </div>
            )}
          </div>

          <div className="flex items-center gap-1 md:gap-2">
            <button onClick={() => nav("catalog")} className="sm:hidden p-2 rounded-full hover:bg-white/10 transition-colors"><Search size={19} color={C.cream} /></button>
            <button onClick={() => nav("favorites")} className="relative p-2 rounded-full hover:bg-white/10 transition-colors" aria-label="Favoritos">
              <Heart size={18} color={C.cream} />
              {favCount > 0 && <Badge n={favCount} />}
            </button>
            <button onClick={onCartOpen} className="relative p-2 rounded-full hover:bg-white/10 transition-colors" aria-label="Carrinho">
              <ShoppingBag size={18} color={C.cream} />
              {cartCount > 0 && <Badge n={cartCount} />}
            </button>
            <button onClick={() => (user ? onAccount() : onAuthOpen("login"))} className="p-2 rounded-full hover:bg-white/10 transition-colors" aria-label="Conta">
              <User size={18} color={C.cream} />
            </button>
          </div>
        </div>
      </div>

      {menuOpen && (
        <div className="md:hidden px-4 pb-4 flex flex-col gap-3 border-t" style={{ borderColor: "#ffffff1a" }}>
          <div className="relative mt-3">
            <Search size={15} className="absolute left-3 top-1/2 -translate-y-1/2" color={`${C.cream}88`} />
            <input value={search} onChange={(e) => setSearch(e.target.value)} placeholder="Buscar peças..." className="w-full font-body text-[13px] pl-9 pr-3 py-2 rounded-full outline-none" style={{ background: "#ffffff12", color: C.cream }} />
          </div>
          {[["home", "Início"], ["catalog", "Catálogo"], ["favorites", "Favoritos"]].map(([r, l]) => (
            <button key={r} onClick={() => { nav(r); setMenuOpen(false); }} className="text-left font-body text-sm py-1" style={{ color: C.cream }}>{l}</button>
          ))}
        </div>
      )}
    </header>
  );
}

function Badge({ n }) {
  return (
    <span
      className="absolute -top-0.5 -right-0.5 min-w-[16px] h-4 px-1 rounded-full flex items-center justify-center font-mono text-[9px] font-bold"
      style={{ background: C.brass, color: C.ink }}
    >
      {n}
    </span>
  );
}

/* ------------------------------------------------------------------ */
/* HOME                                                                 */
/* ------------------------------------------------------------------ */
function Home({ products, nav, openProduct, addCart, favorites, toggleFav }) {
  const featured = products.filter((p) => p.featured).slice(0, 4);
  const recent = [...products].sort((a, b) => (a.createdAt < b.createdAt ? 1 : -1)).slice(0, 4);

  return (
    <div>
      {/* HERO */}
      <section className="relative overflow-hidden" style={{ background: C.ink }}>
        <div
          className="absolute inset-0 opacity-[0.06]"
          style={{ backgroundImage: `radial-gradient(circle, ${C.brass} 1px, transparent 1px)`, backgroundSize: "22px 22px" }}
        />
        <div className="max-w-7xl mx-auto px-4 md:px-6 py-16 md:py-28 grid md:grid-cols-[1.05fr_0.95fr] gap-12 md:gap-8 items-center relative">
          <div className="fade-up">
            <div className="inline-flex items-center gap-2 mb-6 px-3 py-1.5 rounded-full border" style={{ borderColor: "#ffffff26" }}>
              <span className="w-1.5 h-1.5 rounded-full" style={{ background: C.brass }} />
              <p className="font-mono text-[10.5px] tracking-[0.18em] uppercase" style={{ color: C.brass }}>Curadoria de segunda mão</p>
            </div>
            <h1 className="font-display text-[15vw] leading-[0.97] sm:text-[3.4rem] md:text-[3.6rem]" style={{ color: C.cream }}>
              Roupas com<br /><span className="italic" style={{ color: C.brass }}>história</span>, prontas<br />pra outra história
            </h1>
            <p className="font-body text-[15px] mt-7 max-w-md leading-relaxed" style={{ color: `${C.cream}b3` }}>
              Cada peça passa por seleção cuidadosa antes de chegar até você — e, como é única, quando vende, sai do catálogo. Sem reposição, sem igual.
            </p>
            <div className="flex flex-wrap items-center gap-4 mt-9">
              <button onClick={() => nav("catalog")} className="btn-lift font-body text-sm font-medium px-6 py-3.5 rounded-full shadow-lg" style={{ background: C.brass, color: C.ink, boxShadow: "0 12px 24px -10px #B08D5766" }}>
                Ver catálogo
              </button>
              <button onClick={() => nav("catalog")} className="hover-underline font-body text-sm px-1 py-3.5" style={{ color: C.cream }}>
                Recém-chegadas →
              </button>
            </div>
            <div className="flex items-center gap-6 mt-10 pt-6 border-t" style={{ borderColor: "#ffffff1a" }}>
              {[["+300", "peças já circularam"], ["100%", "curadoria manual"], ["Pix", "pagamento único"]].map(([n, l]) => (
                <div key={l}>
                  <p className="font-display text-lg" style={{ color: C.cream }}>{n}</p>
                  <p className="font-body text-[10.5px] leading-tight max-w-[7rem]" style={{ color: `${C.cream}80` }}>{l}</p>
                </div>
              ))}
            </div>
          </div>

          <div className="relative fade-up" style={{ animationDelay: "0.12s" }}>
            <div className="grid grid-cols-2 gap-3.5">
              {products.slice(0, 4).map((p, i) => (
                <div
                  key={p.id}
                  className={`aspect-[3/4] rounded-md overflow-hidden shadow-2xl ${i % 2 === 1 ? "mt-9" : ""}`}
                  style={{ transform: `rotate(${i % 2 === 0 ? -1.5 : 1.5}deg)` }}
                >
                  <PhotoPanel product={p} variant={i} className="w-full h-full" />
                </div>
              ))}
            </div>
            <div
              className="absolute -bottom-5 -left-5 md:-left-8 w-24 h-24 rounded-full flex flex-col items-center justify-center text-center shadow-xl"
              style={{ background: C.burgundy, transform: "rotate(-8deg)" }}
            >
              <span className="font-display italic text-[13px] leading-tight" style={{ color: C.cream }}>peça</span>
              <span className="font-display italic text-[13px] leading-tight" style={{ color: C.cream }}>única</span>
            </div>
          </div>
        </div>
      </section>

      {/* CATEGORIES */}
      <section className="max-w-7xl mx-auto px-4 md:px-6 py-14">
        <p className="font-mono text-[10.5px] tracking-[0.18em] uppercase mb-2" style={{ color: C.brass }}>Explore</p>
        <h2 className="font-display text-3xl mb-7" style={{ color: C.ink }}>Categorias</h2>
        <div className="flex gap-3 overflow-x-auto scrollbar-thin pb-2">
          {CATEGORIES.map((c) => {
            const Icon = iconFor(c);
            return (
              <button
                key={c}
                onClick={() => nav("catalog", { category: c })}
                className="btn-lift shrink-0 flex flex-col items-center gap-2.5 px-6 py-5 rounded-md border"
                style={{ borderColor: "#1C262018", background: C.cream }}
              >
                <Icon size={21} color={C.forest} strokeWidth={1.3} />
                <span className="font-body text-[12px]" style={{ color: C.ink }}>{c}</span>
              </button>
            );
          })}
        </div>
      </section>

      <div className="max-w-7xl mx-auto px-4 md:px-6"><div className="stitch" style={{ color: C.ink }} /></div>

      {/* FEATURED */}
      <section className="max-w-7xl mx-auto px-4 md:px-6 py-14">
        <div className="flex items-end justify-between mb-7">
          <div>
            <p className="font-mono text-[10.5px] tracking-[0.18em] uppercase mb-2" style={{ color: C.brass }}>Curadoria da semana</p>
            <h2 className="font-display text-3xl" style={{ color: C.ink }}>Em destaque</h2>
          </div>
          <button onClick={() => nav("catalog")} className="hover-underline font-body text-[12px] flex items-center gap-1 shrink-0" style={{ color: C.burgundy }}>
            Ver tudo <ChevronRight size={14} />
          </button>
        </div>
        <div className="grid grid-cols-2 md:grid-cols-4 gap-5 md:gap-7">
          {featured.map((p, i) => (
            <ProductCard key={p.id} product={p} index={i} onOpen={openProduct} onAddCart={addCart} isFav={favorites.has(p.id)} onToggleFav={toggleFav} />
          ))}
        </div>
      </section>

      {/* RECENT */}
      <section className="max-w-7xl mx-auto px-4 md:px-6 py-14">
        <div className="mb-7">
          <p className="font-mono text-[10.5px] tracking-[0.18em] uppercase mb-2" style={{ color: C.brass }}>Acabaram de chegar</p>
          <h2 className="font-display text-3xl" style={{ color: C.ink }}>Novidades no brechó</h2>
        </div>
        <div className="grid grid-cols-2 md:grid-cols-4 gap-5 md:gap-7">
          {recent.map((p, i) => (
            <ProductCard key={p.id} product={p} index={i + 2} onOpen={openProduct} onAddCart={addCart} isFav={favorites.has(p.id)} onToggleFav={toggleFav} />
          ))}
        </div>
      </section>

      {/* ABOUT STRIP */}
      <section className="mt-6 grain" style={{ background: C.forest }}>
        <div className="max-w-7xl mx-auto px-4 md:px-6 py-16 grid md:grid-cols-3 gap-10">
          {[
            [Gem, "Peças únicas", "Cada item existe em unidade só — quando vende, some do catálogo, sem reposição."],
            [Star, "Curadoria manual", "Selecionamos marca, tecido e estado antes de qualquer peça entrar no site."],
            [BagIcon, "Pagamento via Pix", "Compra simples, QR Code na hora, confirmação rápida e sem burocracia."],
          ].map(([Icon, t, d], i) => (
            <div key={t} className="fade-up" style={{ animationDelay: `${i * 0.08}s` }}>
              <div className="w-10 h-10 rounded-full flex items-center justify-center mb-4" style={{ background: "#ffffff12" }}>
                <Icon size={17} color={C.brass} strokeWidth={1.5} />
              </div>
              <p className="font-display text-xl mb-2" style={{ color: C.cream }}>{t}</p>
              <p className="font-body text-[13px] leading-relaxed" style={{ color: `${C.cream}9c` }}>{d}</p>
            </div>
          ))}
        </div>
      </section>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* CATALOG                                                              */
/* ------------------------------------------------------------------ */
const emptyFilters = { category: [], brand: [], color: [], size: [], gender: [], condition: [], min: "", max: "" };

function Catalog({ products, initialFilters, openProduct, addCart, favorites, toggleFav, search, setSearch }) {
  const [filters, setFilters] = useState({ ...emptyFilters, ...(initialFilters || {}) });
  const [sort, setSort] = useState("recent");
  const [filtersOpen, setFiltersOpen] = useState(false);

  useEffect(() => {
    if (initialFilters?.category) setFilters((f) => ({ ...f, category: [initialFilters.category] }));
  }, [initialFilters]);

  const toggle = (key, val) => setFilters((f) => ({ ...f, [key]: f[key].includes(val) ? f[key].filter((v) => v !== val) : [...f[key], val] }));

  const filtered = useMemo(() => {
    let list = products.filter((p) => {
      const q = search.trim().toLowerCase();
      const matchesSearch = !q || [p.name, p.brand, p.category, p.color, p.size, p.description].join(" ").toLowerCase().includes(q);
      const inCat = !filters.category.length || filters.category.includes(p.category);
      const inBrand = !filters.brand.length || filters.brand.includes(p.brand);
      const inColor = !filters.color.length || filters.color.includes(p.color);
      const inSize = !filters.size.length || filters.size.includes(p.size);
      const inGender = !filters.gender.length || filters.gender.includes(p.gender);
      const inCond = !filters.condition.length || filters.condition.includes(p.condition);
      const min = filters.min ? Number(filters.min) : 0;
      const max = filters.max ? Number(filters.max) : Infinity;
      const inPrice = p.price >= min && p.price <= max;
      return matchesSearch && inCat && inBrand && inColor && inSize && inGender && inCond && inPrice;
    });
    switch (sort) {
      case "lowest": list.sort((a, b) => a.price - b.price); break;
      case "highest": list.sort((a, b) => b.price - a.price); break;
      case "recent": list.sort((a, b) => (a.createdAt < b.createdAt ? 1 : -1)); break;
      case "oldest": list.sort((a, b) => (a.createdAt > b.createdAt ? 1 : -1)); break;
      case "bestseller": list.sort((a, b) => b.sold - a.sold); break;
      case "az": list.sort((a, b) => a.name.localeCompare(b.name)); break;
      default: break;
    }
    return list;
  }, [products, filters, sort, search]);

  const sizes = [...new Set(products.map((p) => p.size))];
  const colors = [...new Set(products.map((p) => p.color))];

  const FilterGroup = ({ title, options, keyName, swatches }) => (
    <div className="mb-6">
      <p className="font-body text-[12px] font-semibold tracking-wide uppercase mb-2.5" style={{ color: C.ink }}>{title}</p>
      <div className="flex flex-wrap gap-2">
        {options.map((o) => {
          const active = filters[keyName].includes(o);
          return (
            <button
              key={o}
              onClick={() => toggle(keyName, o)}
              className="flex items-center gap-1.5 px-2.5 py-1.5 rounded-full border font-body text-[12px]"
              style={{
                borderColor: active ? C.ink : "#1C262030",
                background: active ? C.ink : "transparent",
                color: active ? C.cream : C.ink,
              }}
            >
              {swatches && <span className="w-2.5 h-2.5 rounded-full border" style={{ background: COLOR_MAP[o] || "#ccc", borderColor: "#0002" }} />}
              {o}
            </button>
          );
        })}
      </div>
    </div>
  );

  const FiltersPanel = (
    <div>
      <FilterGroup title="Categoria" options={CATEGORIES} keyName="category" />
      <FilterGroup title="Marca" options={BRANDS} keyName="brand" />
      <FilterGroup title="Cor" options={colors} keyName="color" swatches />
      <FilterGroup title="Tamanho" options={sizes} keyName="size" />
      <FilterGroup title="Gênero" options={GENDERS} keyName="gender" />
      <FilterGroup title="Estado" options={CONDITIONS} keyName="condition" />
      <div className="mb-4">
        <p className="font-body text-[12px] font-semibold tracking-wide uppercase mb-2.5" style={{ color: C.ink }}>Faixa de preço</p>
        <div className="flex items-center gap-2">
          <input value={filters.min} onChange={(e) => setFilters((f) => ({ ...f, min: e.target.value }))} placeholder="Mín." type="number" className="w-full font-mono text-[12px] px-2.5 py-1.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }} />
          <span style={{ color: C.ink }}>–</span>
          <input value={filters.max} onChange={(e) => setFilters((f) => ({ ...f, max: e.target.value }))} placeholder="Máx." type="number" className="w-full font-mono text-[12px] px-2.5 py-1.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }} />
        </div>
      </div>
      <button onClick={() => setFilters(emptyFilters)} className="font-body text-[12px] underline" style={{ color: C.burgundy }}>Limpar filtros</button>
    </div>
  );

  return (
    <div className="max-w-7xl mx-auto px-4 md:px-6 py-8">
      <div className="flex items-center justify-between mb-6 gap-3">
        <div>
          <h1 className="font-display text-3xl" style={{ color: C.ink }}>Catálogo</h1>
          <p className="font-body text-[12px] mt-1" style={{ color: "#5B5346" }}>{filtered.length} peça{filtered.length !== 1 ? "s" : ""} disponíve{filtered.length !== 1 ? "is" : "l"}</p>
        </div>
        <div className="flex items-center gap-2">
          <button onClick={() => setFiltersOpen(true)} className="lg:hidden flex items-center gap-1.5 font-body text-[12px] px-3 py-2 rounded-full border" style={{ borderColor: "#1C262030" }}>
            <Filter size={13} /> Filtros
          </button>
          <select value={sort} onChange={(e) => setSort(e.target.value)} className="font-body text-[12px] px-3 py-2 rounded-full border outline-none" style={{ borderColor: "#1C262030", color: C.ink, background: C.parchment }}>
            <option value="recent">Mais recentes</option>
            <option value="oldest">Mais antigos</option>
            <option value="lowest">Menor preço</option>
            <option value="highest">Maior preço</option>
            <option value="bestseller">Mais vendidos</option>
            <option value="az">Ordem alfabética</option>
          </select>
        </div>
      </div>

      <div className="grid lg:grid-cols-[220px_1fr] gap-8">
        <aside className="hidden lg:block">{FiltersPanel}</aside>

        {filtersOpen && (
          <div className="fixed inset-0 z-50 lg:hidden">
            <div className="absolute inset-0 bg-black/40" onClick={() => setFiltersOpen(false)} />
            <div className="absolute right-0 top-0 bottom-0 w-[82%] max-w-xs p-5 overflow-y-auto" style={{ background: C.cream }}>
              <div className="flex justify-between items-center mb-5">
                <p className="font-display text-lg" style={{ color: C.ink }}>Filtros</p>
                <button onClick={() => setFiltersOpen(false)}><X size={18} color={C.ink} /></button>
              </div>
              {FiltersPanel}
              <button onClick={() => setFiltersOpen(false)} className="w-full mt-4 py-2.5 rounded-full font-body text-sm" style={{ background: C.ink, color: C.cream }}>Aplicar</button>
            </div>
          </div>
        )}

        <div>
          {filtered.length === 0 ? (
            <div className="text-center py-20">
              <p className="font-display text-xl mb-2" style={{ color: C.ink }}>Nenhuma peça encontrada</p>
              <p className="font-body text-[13px]" style={{ color: "#5B5346" }}>Tente ajustar os filtros ou buscar por outro termo.</p>
            </div>
          ) : (
            <div className="grid grid-cols-2 md:grid-cols-3 gap-5 md:gap-6">
              {filtered.map((p, i) => (
                <ProductCard key={p.id} product={p} index={i} onOpen={openProduct} onAddCart={addCart} isFav={favorites.has(p.id)} onToggleFav={toggleFav} />
              ))}
            </div>
          )}
        </div>
      </div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* PRODUCT DETAIL                                                       */
/* ------------------------------------------------------------------ */
function ProductDetail({ product, products, back, addCart, buyNow, favorites, toggleFav, openProduct }) {
  const [imgIdx, setImgIdx] = useState(0);
  const photos = [0, 1, 2, 3, 4];
  const related = products.filter((p) => p.id !== product.id && p.category === product.category).slice(0, 4);
  const isFav = favorites.has(product.id);

  return (
    <div className="max-w-7xl mx-auto px-4 md:px-6 py-8">
      <button onClick={back} className="flex items-center gap-1.5 font-body text-[12px] mb-6" style={{ color: "#5B5346" }}>
        <ArrowLeft size={14} /> Voltar
      </button>
      <div className="grid md:grid-cols-2 gap-10">
        <div>
          <div className="aspect-[4/5] rounded-md overflow-hidden mb-3 shadow-lg">
            <PhotoPanel product={product} variant={imgIdx} className="w-full h-full" />
          </div>
          <div className="flex gap-2.5">
            {photos.map((i) => (
              <button key={i} onClick={() => setImgIdx(i)} className="btn-lift w-16 aspect-[4/5] rounded-sm overflow-hidden border-2" style={{ borderColor: imgIdx === i ? C.brass : "transparent" }}>
                <PhotoPanel product={product} variant={i} className="w-full h-full" />
              </button>
            ))}
          </div>
        </div>

        <div>
          <p className="font-mono text-[11px] tracking-widest uppercase" style={{ color: C.brass }}>{product.brand}</p>
          <div className="flex items-start justify-between gap-3 mt-1">
            <h1 className="font-display text-3xl leading-tight" style={{ color: C.ink }}>{product.name}</h1>
            <button onClick={() => toggleFav(product.id)} className="w-10 h-10 rounded-full flex items-center justify-center border shrink-0" style={{ borderColor: "#1C262030" }}>
              <Heart size={17} fill={isFav ? C.burgundy : "none"} color={isFav ? C.burgundy : C.ink} />
            </button>
          </div>

          <div className="mt-4"><PriceTag price={product.price} /></div>

          <p className="font-body text-[14px] leading-relaxed mt-5" style={{ color: "#3C3626" }}>{product.description}</p>

          <div className="grid grid-cols-2 gap-3 mt-6">
            {[["Categoria", product.category], ["Cor", product.color], ["Tamanho", product.size], ["Estado", product.condition], ["Gênero", product.gender]].map(([k, v]) => (
              <div key={k} className="border-t pt-2" style={{ borderColor: "#1C262022" }}>
                <p className="font-mono text-[10px] uppercase tracking-wide" style={{ color: "#5B5346" }}>{k}</p>
                <p className="font-body text-[13px]" style={{ color: C.ink }}>{v}</p>
              </div>
            ))}
          </div>

          <div className="flex gap-3 mt-8">
            <button onClick={() => buyNow(product.id)} className="btn-lift flex-1 py-3.5 rounded-full font-body text-sm font-medium shadow-lg" style={{ background: C.burgundy, color: C.cream, boxShadow: "0 14px 26px -12px #7A2E2E66" }}>
              Comprar agora
            </button>
            <button onClick={() => addCart(product.id)} className="btn-lift flex-1 py-3.5 rounded-full font-body text-sm border-[1.5px]" style={{ borderColor: C.ink, color: C.ink }}>
              Adicionar ao carrinho
            </button>
          </div>
          <p className="font-body text-[11px] mt-3" style={{ color: "#5B5346" }}>Peça única · pagamento via Pix · após confirmação a peça sai do catálogo.</p>
        </div>
      </div>

      {related.length > 0 && (
        <div className="mt-16">
          <h2 className="font-display text-2xl mb-6" style={{ color: C.ink }}>Você também pode gostar</h2>
          <div className="grid grid-cols-2 md:grid-cols-4 gap-5 md:gap-6">
            {related.map((p, i) => (
              <ProductCard key={p.id} product={p} index={i} onOpen={openProduct} onAddCart={addCart} isFav={favorites.has(p.id)} onToggleFav={toggleFav} />
            ))}
          </div>
        </div>
      )}
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* FAVORITES PAGE                                                       */
/* ------------------------------------------------------------------ */
function FavoritesPage({ products, favorites, openProduct, addCart, toggleFav }) {
  const list = products.filter((p) => favorites.has(p.id));
  return (
    <div className="max-w-7xl mx-auto px-4 md:px-6 py-8">
      <h1 className="font-display text-3xl mb-6" style={{ color: C.ink }}>Favoritos</h1>
      {list.length === 0 ? (
        <p className="font-body text-[13px]" style={{ color: "#5B5346" }}>Você ainda não favoritou nenhuma peça.</p>
      ) : (
        <div className="grid grid-cols-2 md:grid-cols-4 gap-5 md:gap-6">
          {list.map((p, i) => (
            <ProductCard key={p.id} product={p} index={i} onOpen={openProduct} onAddCart={addCart} isFav={true} onToggleFav={toggleFav} />
          ))}
        </div>
      )}
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* CART DRAWER                                                          */
/* ------------------------------------------------------------------ */
function CartDrawer({ open, close, items, products, removeItem, checkout }) {
  const list = items.map((id) => products.find((p) => p.id === id)).filter(Boolean);
  const subtotal = list.reduce((s, p) => s + p.price, 0);

  if (!open) return null;
  return (
    <div className="fixed inset-0 z-50">
      <div className="absolute inset-0 bg-black/40" onClick={close} />
      <div className="absolute right-0 top-0 bottom-0 w-full max-w-sm flex flex-col" style={{ background: C.cream }}>
        <div className="flex items-center justify-between p-5 border-b" style={{ borderColor: "#1C262022" }}>
          <p className="font-display text-xl" style={{ color: C.ink }}>Seu carrinho</p>
          <button onClick={close}><X size={19} color={C.ink} /></button>
        </div>

        <div className="flex-1 overflow-y-auto p-5 scrollbar-thin">
          {list.length === 0 ? (
            <p className="font-body text-[13px]" style={{ color: "#5B5346" }}>Seu carrinho está vazio.</p>
          ) : (
            <div className="flex flex-col gap-4">
              {list.map((p) => (
                <div key={p.id} className="flex gap-3">
                  <div className="w-16 h-20 rounded-sm overflow-hidden shrink-0"><PhotoPanel product={p} className="w-full h-full" /></div>
                  <div className="flex-1 min-w-0">
                    <p className="font-body text-[13px] leading-tight" style={{ color: C.ink }}>{p.name}</p>
                    <p className="font-mono text-[10px] mt-0.5" style={{ color: C.brass }}>{p.brand} · {p.size}</p>
                    <p className="font-body text-[11px] mt-0.5" style={{ color: "#5B5346" }}>Peça única · qtd. 1</p>
                    <p className="font-mono text-[13px] font-bold mt-1" style={{ color: C.ink }}>{brl(p.price)}</p>
                  </div>
                  <button onClick={() => removeItem(p.id)} aria-label="Remover"><Trash2 size={15} color={C.burgundy} /></button>
                </div>
              ))}
            </div>
          )}
        </div>

        {list.length > 0 && (
          <div className="p-5 border-t" style={{ borderColor: "#1C262022" }}>
            <div className="flex justify-between font-body text-sm mb-4" style={{ color: C.ink }}>
              <span>Subtotal</span>
              <span className="font-mono font-bold">{brl(subtotal)}</span>
            </div>
            <button onClick={checkout} className="btn-lift w-full py-3.5 rounded-full font-body text-sm font-medium shadow-lg" style={{ background: C.burgundy, color: C.cream, boxShadow: "0 14px 26px -12px #7A2E2E66" }}>
              Finalizar compra
            </button>
          </div>
        )}
      </div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* CHECKOUT / PIX MODAL                                                 */
/* ------------------------------------------------------------------ */
function pseudoQR(seed) {
  let h = 0;
  for (let i = 0; i < seed.length; i++) h = (h * 31 + seed.charCodeAt(i)) >>> 0;
  const cells = [];
  for (let i = 0; i < 121; i++) {
    h = (h * 1103515245 + 12345) >>> 0;
    cells.push((h >> 16) % 3 === 0);
  }
  return cells;
}

function CheckoutModal({ open, close, items, products, confirmPayment }) {
  const [copied, setCopied] = useState(false);
  const [status, setStatus] = useState("pending"); // pending | confirming | done
  const list = items.map((id) => products.find((p) => p.id === id)).filter(Boolean);
  const subtotal = list.reduce((s, p) => s + p.price, 0);
  const pixKey = "brechodutra@pix.com.br";
  const seed = items.join("-") + subtotal;
  const cells = useMemo(() => pseudoQR(seed || "brecho"), [seed]);

  useEffect(() => { if (open) setStatus("pending"); }, [open]);

  if (!open) return null;

  const handleConfirm = () => {
    setStatus("confirming");
    setTimeout(() => {
      setStatus("done");
      confirmPayment();
    }, 1400);
  };

  return (
    <div className="fixed inset-0 z-[60] flex items-center justify-center p-4">
      <div className="absolute inset-0 bg-black/50" onClick={status === "done" ? close : undefined} />
      <div className="relative w-full max-w-sm rounded-md overflow-hidden" style={{ background: C.cream }}>
        {status !== "done" && (
          <button onClick={close} className="absolute top-3 right-3 z-10"><X size={18} color={C.ink} /></button>
        )}
        <div className="p-6">
          {status !== "done" ? (
            <>
              <p className="font-display text-xl mb-1" style={{ color: C.ink }}>Pagamento via Pix</p>
              <p className="font-body text-[12px] mb-5" style={{ color: "#5B5346" }}>Escaneie o QR Code ou copie a chave abaixo.</p>

              <div className="mx-auto w-44 h-44 grid grid-cols-11 grid-rows-11 gap-[1px] p-2 rounded-sm border" style={{ background: "#fff", borderColor: "#1C262022" }}>
                {cells.map((on, i) => (
                  <div key={i} style={{ background: on ? C.ink : "transparent" }} />
                ))}
              </div>
              <p className="font-mono text-[9px] text-center mt-1.5" style={{ color: "#5B5346" }}>QR Code ilustrativo</p>

              <div className="mt-5 flex items-center gap-2 border rounded-full px-3 py-2" style={{ borderColor: "#1C262030" }}>
                <span className="font-mono text-[12px] flex-1 truncate" style={{ color: C.ink }}>{pixKey}</span>
                <button
                  onClick={() => { navigator.clipboard?.writeText(pixKey); setCopied(true); setTimeout(() => setCopied(false), 1500); }}
                  className="flex items-center gap-1 font-body text-[11px] px-2 py-1 rounded-full"
                  style={{ background: C.ink, color: C.cream }}
                >
                  {copied ? <Check size={12} /> : <Copy size={12} />} {copied ? "Copiado" : "Copiar"}
                </button>
              </div>

              <div className="mt-5 space-y-1.5">
                {list.map((p) => (
                  <div key={p.id} className="flex justify-between font-body text-[12px]" style={{ color: "#3C3626" }}>
                    <span className="truncate pr-2">{p.name}</span><span className="font-mono shrink-0">{brl(p.price)}</span>
                  </div>
                ))}
              </div>
              <div className="flex justify-between font-body text-sm font-semibold mt-3 pt-3 border-t" style={{ borderColor: "#1C262022", color: C.ink }}>
                <span>Total</span><span className="font-mono">{brl(subtotal)}</span>
              </div>

              <button
                onClick={handleConfirm}
                disabled={status === "confirming"}
                className="w-full mt-6 py-3.5 rounded-full font-body text-sm font-medium disabled:opacity-60"
                style={{ background: C.burgundy, color: C.cream }}
              >
                {status === "confirming" ? "Confirmando pagamento..." : "Já paguei / Confirmar pagamento"}
              </button>
              <p className="font-body text-[10px] text-center mt-2" style={{ color: "#5B5346" }}>Simulação de confirmação — em produção isto viria de um webhook do provedor Pix.</p>
            </>
          ) : (
            <div className="text-center py-4">
              <div className="w-14 h-14 mx-auto rounded-full flex items-center justify-center mb-4" style={{ background: C.forest }}>
                <Check size={26} color={C.cream} />
              </div>
              <p className="font-display text-xl mb-1" style={{ color: C.ink }}>Pagamento confirmado!</p>
              <p className="font-body text-[13px] mb-6" style={{ color: "#5B5346" }}>Sua compra foi registrada e as peças já saíram do catálogo.</p>
              <button onClick={close} className="w-full py-3 rounded-full font-body text-sm" style={{ background: C.ink, color: C.cream }}>Continuar</button>
            </div>
          )}
        </div>
      </div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* AUTH MODAL                                                           */
/* ------------------------------------------------------------------ */
function AuthModal({ mode, setMode, close, login }) {
  const [name, setName] = useState("");
  const [email, setEmail] = useState("");
  const [pw, setPw] = useState("");
  const [err, setErr] = useState("");

  if (!mode) return null;

  const submit = () => {
    if (mode === "register" && !name.trim()) return setErr("Informe seu nome.");
    if (!email.includes("@")) return setErr("Informe um e-mail válido.");
    if (mode !== "forgot" && pw.length < 4) return setErr("Senha deve ter ao menos 4 caracteres.");
    setErr("");
    if (mode === "forgot") { setMode("resetSent"); return; }
    login({ name: name || email.split("@")[0], email });
  };

  return (
    <div className="fixed inset-0 z-[60] flex items-center justify-center p-4">
      <div className="absolute inset-0 bg-black/50" onClick={close} />
      <div className="relative w-full max-w-sm rounded-md p-6" style={{ background: C.cream }}>
        <button onClick={close} className="absolute top-3 right-3"><X size={18} color={C.ink} /></button>

        {mode === "resetSent" ? (
          <div className="text-center py-4">
            <p className="font-display text-xl mb-2" style={{ color: C.ink }}>Verifique seu e-mail</p>
            <p className="font-body text-[13px] mb-5" style={{ color: "#5B5346" }}>Enviamos um link de recuperação de senha para {email}.</p>
            <button onClick={() => setMode("login")} className="font-body text-[12px] underline" style={{ color: C.burgundy }}>Voltar ao login</button>
          </div>
        ) : (
          <>
            <p className="font-display text-xl mb-5" style={{ color: C.ink }}>
              {mode === "login" ? "Entrar na conta" : mode === "register" ? "Criar conta" : "Recuperar senha"}
            </p>
            <div className="flex flex-col gap-3">
              {mode === "register" && (
                <Input label="Nome" value={name} onChange={setName} />
              )}
              <Input label="E-mail" value={email} onChange={setEmail} type="email" />
              {mode !== "forgot" && <Input label="Senha" value={pw} onChange={setPw} type="password" />}
              {err && <p className="font-body text-[12px]" style={{ color: C.burgundy }}>{err}</p>}
              <button onClick={submit} className="w-full py-3 rounded-full font-body text-sm mt-1" style={{ background: C.ink, color: C.cream }}>
                {mode === "login" ? "Entrar" : mode === "register" ? "Criar conta" : "Enviar link"}
              </button>
            </div>

            <div className="mt-4 flex flex-col gap-1.5 text-center">
              {mode === "login" && (
                <>
                  <button onClick={() => setMode("forgot")} className="font-body text-[12px] underline" style={{ color: "#5B5346" }}>Esqueci minha senha</button>
                  <button onClick={() => setMode("register")} className="font-body text-[12px]" style={{ color: "#5B5346" }}>Não tem conta? <span className="underline" style={{ color: C.burgundy }}>Criar agora</span></button>
                </>
              )}
              {mode === "register" && (
                <button onClick={() => setMode("login")} className="font-body text-[12px]" style={{ color: "#5B5346" }}>Já tem conta? <span className="underline" style={{ color: C.burgundy }}>Entrar</span></button>
              )}
              {mode === "forgot" && (
                <button onClick={() => setMode("login")} className="font-body text-[12px] underline" style={{ color: "#5B5346" }}>Voltar ao login</button>
              )}
            </div>
            <p className="font-body text-[10px] text-center mt-4" style={{ color: "#8a8272" }}>Dica: use e-mail com "admin" para acessar o painel administrativo de demonstração.</p>
          </>
        )}
      </div>
    </div>
  );
}

function Input({ label, value, onChange, type = "text" }) {
  return (
    <label className="block">
      <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>{label}</span>
      <input value={value} onChange={(e) => onChange(e.target.value)} type={type} className="w-full mt-1 font-body text-[13px] px-3 py-2.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }} />
    </label>
  );
}

/* ------------------------------------------------------------------ */
/* ACCOUNT AREA                                                         */
/* ------------------------------------------------------------------ */
function AccountPage({ user, orders, favorites, products, logout, nav }) {
  const [tab, setTab] = useState("orders");
  const myOrders = orders.filter((o) => o.email === user.email);
  const favList = products.filter((p) => favorites.has(p.id));

  const tabs = [
    ["orders", "Meus pedidos", ClipboardList],
    ["history", "Histórico de compras", Package],
    ["favorites", "Favoritos", Heart],
    ["profile", "Dados pessoais", User],
  ];

  return (
    <div className="max-w-5xl mx-auto px-4 md:px-6 py-8">
      <h1 className="font-display text-3xl mb-6" style={{ color: C.ink }}>Minha conta</h1>
      <div className="grid md:grid-cols-[200px_1fr] gap-8">
        <div className="flex md:flex-col gap-1 overflow-x-auto">
          {tabs.map(([k, l, Icon]) => (
            <button key={k} onClick={() => setTab(k)} className="flex items-center gap-2 shrink-0 px-3 py-2.5 rounded-sm font-body text-[13px] text-left" style={{ background: tab === k ? C.parchment : "transparent", color: C.ink }}>
              <Icon size={14} /> {l}
            </button>
          ))}
          <button onClick={() => { logout(); nav("home"); }} className="flex items-center gap-2 px-3 py-2.5 font-body text-[13px]" style={{ color: C.burgundy }}>
            <LogOut size={14} /> Sair da conta
          </button>
        </div>

        <div>
          {(tab === "orders" || tab === "history") && (
            myOrders.length === 0 ? (
              <p className="font-body text-[13px]" style={{ color: "#5B5346" }}>Nenhum pedido por aqui ainda.</p>
            ) : (
              <div className="flex flex-col gap-3">
                {myOrders.map((o) => (
                  <div key={o.id} className="border rounded-sm p-4" style={{ borderColor: "#1C262022" }}>
                    <div className="flex justify-between font-body text-[13px]" style={{ color: C.ink }}>
                      <span>Pedido #{o.id}</span>
                      <span className="font-mono font-bold">{brl(o.total)}</span>
                    </div>
                    <p className="font-body text-[11px] mt-1" style={{ color: "#5B5346" }}>{o.date} · {o.items.length} peça(s) · <span style={{ color: C.forest }}>{o.status}</span></p>
                  </div>
                ))}
              </div>
            )
          )}
          {tab === "favorites" && (
            favList.length === 0 ? <p className="font-body text-[13px]" style={{ color: "#5B5346" }}>Nenhum favorito.</p> :
            <div className="grid grid-cols-2 sm:grid-cols-3 gap-4">
              {favList.map((p) => (
                <div key={p.id} className="aspect-[4/5] rounded-sm overflow-hidden"><PhotoPanel product={p} className="w-full h-full" /></div>
              ))}
            </div>
          )}
          {tab === "profile" && (
            <div className="flex flex-col gap-3 max-w-sm">
              <Input label="Nome" value={user.name} onChange={() => {}} />
              <Input label="E-mail" value={user.email} onChange={() => {}} />
              <Input label="Endereço" value={user.address || ""} onChange={() => {}} />
              <button className="w-full py-2.5 rounded-full font-body text-sm mt-1" style={{ background: C.ink, color: C.cream }}>Salvar alterações</button>
            </div>
          )}
        </div>
      </div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* FOOTER                                                               */
/* ------------------------------------------------------------------ */
function Footer({ nav }) {
  return (
    <footer style={{ background: C.ink }}>
      <div className="max-w-7xl mx-auto px-4 md:px-6"><div className="stitch" style={{ color: C.brass }} /></div>
      <div className="max-w-7xl mx-auto px-4 md:px-6 py-16 grid sm:grid-cols-2 md:grid-cols-4 gap-10">
        <div>
          <div className="flex items-center gap-2 mb-3.5">
            <span className="w-7 h-7 rounded-full flex items-center justify-center font-display text-[13px]" style={{ background: C.brass, color: C.ink }}>D</span>
            <p className="font-display text-xl" style={{ color: C.cream }}>Brechó <span className="italic" style={{ color: C.brass }}>Dutra</span></p>
          </div>
          <p className="font-body text-[12px] leading-relaxed max-w-[220px]" style={{ color: `${C.cream}8f` }}>Moda circular com curadoria — peças únicas, selecionadas com carinho.</p>
        </div>
        <div>
          <p className="font-mono text-[10.5px] uppercase tracking-[0.14em] mb-4" style={{ color: C.brass }}>Navegação</p>
          <div className="flex flex-col gap-2.5">
            {[["home", "Início"], ["catalog", "Catálogo"], ["favorites", "Favoritos"]].map(([r, l]) => (
              <button key={r} onClick={() => nav(r)} className="hover-underline font-body text-[13px] text-left w-fit" style={{ color: `${C.cream}b3` }}>{l}</button>
            ))}
          </div>
        </div>
        <div>
          <p className="font-mono text-[10.5px] uppercase tracking-[0.14em] mb-4" style={{ color: C.brass }}>Contato</p>
          <div className="flex flex-col gap-2.5 font-body text-[13px]" style={{ color: `${C.cream}b3` }}>
            <span className="flex items-center gap-2"><MessageCircle size={13} color={C.brass} /> (11) 91234-5678</span>
            <span className="flex items-center gap-2"><MapPin size={13} color={C.brass} /> São Paulo, SP</span>
            <span className="flex items-center gap-2"><Clock size={13} color={C.brass} /> Ter–Sáb, 10h–19h</span>
          </div>
        </div>
        <div>
          <p className="font-mono text-[10.5px] uppercase tracking-[0.14em] mb-4" style={{ color: C.brass }}>Redes sociais</p>
          <div className="flex gap-2.5">
            <span className="btn-lift w-9 h-9 rounded-full flex items-center justify-center cursor-pointer" style={{ background: "#ffffff12" }}><Instagram size={15} color={C.cream} /></span>
            <span className="btn-lift w-9 h-9 rounded-full flex items-center justify-center cursor-pointer" style={{ background: "#ffffff12" }}><MessageCircle size={15} color={C.cream} /></span>
          </div>
        </div>
      </div>
      <div className="border-t py-5 text-center font-mono text-[10px]" style={{ borderColor: "#ffffff12", color: `${C.cream}55` }}>
        © 2026 Brechó Dutra — pagamentos processados exclusivamente via Pix.
      </div>
    </footer>
  );
}

/* ------------------------------------------------------------------ */
/* AI HELPER — calls Claude API for admin content generation & chat     */
/* ------------------------------------------------------------------ */
async function askClaude(prompt, system) {
  try {
    const res = await fetch("https://api.anthropic.com/v1/messages", {
      method: "POST",
      headers: { "Content-Type": "application/json" },
      body: JSON.stringify({
        model: "claude-sonnet-4-6",
        max_tokens: 1000,
        system,
        messages: [{ role: "user", content: prompt }],
      }),
    });
    const data = await res.json();
    const text = (data.content || []).map((b) => b.text || "").join("\n").trim();
    return text || "Não consegui gerar uma resposta agora.";
  } catch (e) {
    return "Erro ao conectar com a IA. Tente novamente.";
  }
}

/* ------------------------------------------------------------------ */
/* ADMIN PANEL                                                          */
/* ------------------------------------------------------------------ */
function AdminPanel({ products, orders, logout }) {
  const [section, setSection] = useState("dashboard");

  const revenueToday = orders.filter((o) => o.date === "01/07/2026").reduce((s, o) => s + o.total, 0);
  const totalRevenue = orders.reduce((s, o) => s + o.total, 0);
  const soldCount = products.reduce((s, p) => s + (p.sold || 0), 0);
  const activeCount = products.length;

  const weekData = [
    { day: "Seg", vendas: 320 }, { day: "Ter", vendas: 480 }, { day: "Qua", vendas: 260 },
    { day: "Qui", vendas: 610 }, { day: "Sex", vendas: 540 }, { day: "Sáb", vendas: 780 }, { day: "Dom", vendas: 390 },
  ];
  const monthData = [
    { mes: "Fev", receita: 3200 }, { mes: "Mar", receita: 4100 }, { mes: "Abr", receita: 3800 },
    { mes: "Mai", receita: 5200 }, { mes: "Jun", receita: 6100 }, { mes: "Jul", receita: 2400 },
  ];

  const navItems = [
    ["dashboard", "Dashboard", LayoutDashboard],
    ["products", "Produtos", Package],
    ["orders", "Pedidos", ClipboardList],
    ["customers", "Clientes", UsersIcon],
    ["ai", "IA — Conteúdo", Sparkles],
  ];

  return (
    <div className="min-h-screen flex" style={{ background: C.parchment }}>
      <aside className="w-56 shrink-0 hidden md:flex flex-col p-5" style={{ background: C.ink }}>
        <p className="font-display text-lg mb-8" style={{ color: C.cream }}>Painel <span style={{ color: C.brass }}>Dutra</span></p>
        <div className="flex flex-col gap-1">
          {navItems.map(([k, l, Icon]) => (
            <button key={k} onClick={() => setSection(k)} className="flex items-center gap-2.5 px-3 py-2.5 rounded-sm font-body text-[13px] text-left" style={{ background: section === k ? "#ffffff14" : "transparent", color: section === k ? C.brass : `${C.cream}cc` }}>
              <Icon size={15} /> {l}
            </button>
          ))}
        </div>
        <button onClick={logout} className="mt-auto flex items-center gap-2.5 px-3 py-2.5 font-body text-[13px]" style={{ color: `${C.cream}99` }}>
          <LogOut size={15} /> Sair do painel
        </button>
      </aside>

      <main className="flex-1 p-5 md:p-8 overflow-y-auto">
        <div className="md:hidden flex gap-2 overflow-x-auto mb-6 pb-1">
          {navItems.map(([k, l, Icon]) => (
            <button key={k} onClick={() => setSection(k)} className="shrink-0 flex items-center gap-1.5 px-3 py-2 rounded-full font-body text-[12px]" style={{ background: section === k ? C.ink : "#1C262014", color: section === k ? C.cream : C.ink }}>
              <Icon size={13} /> {l}
            </button>
          ))}
        </div>

        {section === "dashboard" && (
          <div>
            <h1 className="font-display text-2xl mb-6" style={{ color: C.ink }}>Dashboard</h1>
            <div className="grid grid-cols-2 md:grid-cols-4 gap-4 mb-8">
              {[
                ["Receita hoje", brl(revenueToday || 189)],
                ["Receita semana", brl(2380)],
                ["Receita mês", brl(monthData[monthData.length - 1].receita)],
                ["Total arrecadado", brl(totalRevenue || 24630)],
                ["Pedidos", String(orders.length || 42)],
                ["Produtos cadastrados", String(products.length + soldCount)],
                ["Produtos vendidos", String(soldCount || 95)],
                ["Produtos ativos", String(activeCount)],
              ].map(([l, v]) => (
                <div key={l} className="p-4 rounded-sm border" style={{ background: C.cream, borderColor: "#1C262018" }}>
                  <p className="font-mono text-[10px] uppercase tracking-wide" style={{ color: "#5B5346" }}>{l}</p>
                  <p className="font-display text-xl mt-1" style={{ color: C.ink }}>{v}</p>
                </div>
              ))}
            </div>

            <div className="grid md:grid-cols-2 gap-5">
              <div className="p-4 rounded-sm border" style={{ background: C.cream, borderColor: "#1C262018" }}>
                <p className="font-body text-[13px] font-semibold mb-3" style={{ color: C.ink }}>Vendas na semana</p>
                <ResponsiveContainer width="100%" height={220}>
                  <BarChart data={weekData}>
                    <CartesianGrid strokeDasharray="3 3" stroke="#1C262014" />
                    <XAxis dataKey="day" tick={{ fontSize: 11 }} />
                    <YAxis tick={{ fontSize: 11 }} />
                    <Tooltip />
                    <Bar dataKey="vendas" fill={C.brass} radius={[3, 3, 0, 0]} />
                  </BarChart>
                </ResponsiveContainer>
              </div>
              <div className="p-4 rounded-sm border" style={{ background: C.cream, borderColor: "#1C262018" }}>
                <p className="font-body text-[13px] font-semibold mb-3" style={{ color: C.ink }}>Receita mensal</p>
                <ResponsiveContainer width="100%" height={220}>
                  <LineChart data={monthData}>
                    <CartesianGrid strokeDasharray="3 3" stroke="#1C262014" />
                    <XAxis dataKey="mes" tick={{ fontSize: 11 }} />
                    <YAxis tick={{ fontSize: 11 }} />
                    <Tooltip />
                    <Line type="monotone" dataKey="receita" stroke={C.burgundy} strokeWidth={2.5} dot={{ r: 3 }} />
                  </LineChart>
                </ResponsiveContainer>
              </div>
            </div>
          </div>
        )}

        {section === "products" && <AdminProducts products={products} />}
        {section === "orders" && <AdminOrders orders={orders} />}
        {section === "customers" && <AdminCustomers orders={orders} />}
        {section === "ai" && <AdminAI products={products} />}
      </main>
    </div>
  );
}

const blankProduct = () => ({
  id: null, name: "", brand: "", category: CATEGORIES[0], color: "", size: "",
  gender: GENDERS[0], condition: CONDITIONS[0], price: "", description: "",
  featured: false, createdAt: new Date().toISOString().slice(0, 10), sold: 0, images: [],
});

function AdminProducts({ products, addProduct, updateProduct, deleteProduct }) {
  const [editing, setEditing] = useState(null); // null | product-like object being edited
  const [confirmDelete, setConfirmDelete] = useState(null);

  const openNew = () => setEditing(blankProduct());
  const openEdit = (p) => setEditing({ ...p });

  const save = () => {
    if (!editing.name.trim() || !editing.price) return;
    const payload = { ...editing, price: Number(editing.price) };
    if (payload.id) updateProduct(payload);
    else addProduct({ ...payload, id: "p" + Date.now() });
    setEditing(null);
  };

  return (
    <div>
      <div className="flex items-center justify-between mb-6">
        <div>
          <h1 className="font-display text-2xl" style={{ color: C.ink }}>Produtos</h1>
          <p className="font-body text-[12px] mt-1" style={{ color: "#5B5346" }}>{products.length} peça{products.length !== 1 ? "s" : ""} ativa{products.length !== 1 ? "s" : ""} no catálogo</p>
        </div>
        <button onClick={openNew} className="btn-lift flex items-center gap-1.5 font-body text-[13px] px-4 py-2.5 rounded-full shadow-sm" style={{ background: C.ink, color: C.cream }}>
          <Plus size={14} /> Adicionar produto
        </button>
      </div>

      {products.length === 0 ? (
        <div className="text-center py-20 rounded-md border-2 border-dashed" style={{ borderColor: "#1C262022" }}>
          <Package size={28} className="mx-auto mb-3" color="#8a8272" />
          <p className="font-display text-lg mb-1" style={{ color: C.ink }}>Nenhum produto cadastrado ainda</p>
          <p className="font-body text-[13px] mb-5" style={{ color: "#5B5346" }}>Cadastre a primeira peça real do brechó — a IA ajuda a escrever título e descrição.</p>
          <button onClick={openNew} className="btn-lift inline-flex items-center gap-1.5 font-body text-[13px] px-4 py-2.5 rounded-full" style={{ background: C.brass, color: C.ink }}>
            <Plus size={14} /> Cadastrar peça
          </button>
        </div>
      ) : (
        <div className="rounded-md border overflow-hidden" style={{ borderColor: "#1C262018", background: C.cream }}>
          {products.map((p) => (
            <div key={p.id} className="flex items-center gap-3 px-4 py-3 border-b last:border-0" style={{ borderColor: "#1C262012" }}>
              <div className="w-10 h-12 rounded-sm overflow-hidden shrink-0"><PhotoPanel product={p} className="w-full h-full" /></div>
              <div className="flex-1 min-w-0">
                <p className="font-body text-[13px] truncate" style={{ color: C.ink }}>{p.name}</p>
                <p className="font-mono text-[10px]" style={{ color: "#5B5346" }}>{p.brand || "sem marca"} · {p.category} · {p.condition}</p>
              </div>
              <span className="font-mono text-[13px] font-bold hidden sm:block" style={{ color: C.ink }}>{brl(p.price)}</span>
              <span className="font-mono text-[10px] hidden sm:block" style={{ color: "#5B5346" }}>{p.sold || 0} vend.</span>
              <button onClick={() => openEdit(p)} className="p-2 hover:opacity-70"><Edit2 size={14} color={C.forest} /></button>
              <button onClick={() => setConfirmDelete(p)} className="p-2 hover:opacity-70"><Trash2 size={14} color={C.burgundy} /></button>
            </div>
          ))}
        </div>
      )}

      {editing && (
        <ProductFormModal
          editing={editing}
          setEditing={setEditing}
          onClose={() => setEditing(null)}
          onSave={save}
        />
      )}

      {confirmDelete && (
        <div className="fixed inset-0 z-[60] flex items-center justify-center p-4">
          <div className="absolute inset-0 bg-black/50" onClick={() => setConfirmDelete(null)} />
          <div className="relative w-full max-w-xs rounded-md p-6 text-center" style={{ background: C.cream }}>
            <p className="font-display text-lg mb-2" style={{ color: C.ink }}>Remover peça?</p>
            <p className="font-body text-[12px] mb-5" style={{ color: "#5B5346" }}>"{confirmDelete.name}" será removida do catálogo permanentemente.</p>
            <div className="flex gap-2">
              <button onClick={() => setConfirmDelete(null)} className="flex-1 py-2.5 rounded-full font-body text-[13px] border" style={{ borderColor: "#1C262030", color: C.ink }}>Cancelar</button>
              <button onClick={() => { deleteProduct(confirmDelete.id); setConfirmDelete(null); }} className="flex-1 py-2.5 rounded-full font-body text-[13px]" style={{ background: C.burgundy, color: C.cream }}>Remover</button>
            </div>
          </div>
        </div>
      )}
    </div>
  );
}

function ProductFormModal({ editing, setEditing, onClose, onSave }) {
  const [aiLoading, setAiLoading] = useState(null); // 'titulo' | 'descricao' | 'instagram' | 'whatsapp'
  const [socialText, setSocialText] = useState("");
  const set = (k, v) => setEditing((e) => ({ ...e, [k]: v }));

  const handleFiles = (fileList) => {
    const files = Array.from(fileList).slice(0, 5 - editing.images.length);
    files.forEach((file) => {
      const reader = new FileReader();
      reader.onload = () => setEditing((e) => ({ ...e, images: [...e.images, reader.result].slice(0, 5) }));
      reader.readAsDataURL(file);
    });
  };

  const removeImage = (i) => setEditing((e) => ({ ...e, images: e.images.filter((_, idx) => idx !== i) }));

  const contextLine = () =>
    `${editing.category}, marca ${editing.brand || "não informada"}, cor ${editing.color || "não informada"}, tamanho ${editing.size || "não informado"}, estado ${editing.condition}, preço ${editing.price ? brl(Number(editing.price)) : "a definir"}.`;

  const genField = async (kind) => {
    setAiLoading(kind);
    if (kind === "titulo") {
      const text = await askClaude(`Peça de brechó: ${contextLine()}`, "Você cria títulos curtos e vendáveis para peças de brechó, em português, no máximo 8 palavras, sem aspas.");
      set("name", text.replace(/^"|"$/g, ""));
    } else if (kind === "descricao") {
      const text = await askClaude(`Peça: ${editing.name || "peça de brechó"}. Detalhes: ${contextLine()}`, "Você escreve descrições de produto para um brechó de curadoria chamado Brechó Dutra, tom sofisticado e caloroso, 2-3 frases, em português.");
      set("description", text);
    } else {
      const sys = kind === "instagram"
        ? "Você escreve legendas de Instagram para o Brechó Dutra, tom próximo e estiloso, com 1-2 emojis e hashtags, em português."
        : "Você escreve uma mensagem curta de WhatsApp avisando um cliente sobre esta peça disponível, tom simpático e direto, em português.";
      const text = await askClaude(`Peça: ${editing.name || "peça de brechó"}. Detalhes: ${contextLine()}`, sys);
      setSocialText(text);
    }
    setAiLoading(null);
  };

  return (
    <div className="fixed inset-0 z-[60] flex items-center justify-center p-4">
      <div className="absolute inset-0 bg-black/50" onClick={onClose} />
      <div className="relative w-full max-w-lg rounded-md p-6 max-h-[88vh] overflow-y-auto scrollbar-thin" style={{ background: C.cream }}>
        <button onClick={onClose} className="absolute top-3 right-3"><X size={18} color={C.ink} /></button>
        <p className="font-display text-xl mb-1" style={{ color: C.ink }}>{editing.id ? "Editar produto" : "Novo produto"}</p>
        <p className="font-body text-[12px] mb-5" style={{ color: "#5B5346" }}>Preencha os dados reais da peça e use a IA para agilizar textos.</p>

        <div className="flex flex-col gap-3">
          <div>
            <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>Fotos (até 5)</span>
            <div className="flex flex-wrap gap-2 mt-1.5">
              {editing.images.map((img, i) => (
                <div key={i} className="relative w-16 h-20 rounded-sm overflow-hidden">
                  <img src={img} className="w-full h-full object-cover" alt="" />
                  <button onClick={() => removeImage(i)} className="absolute top-0.5 right-0.5 w-4.5 h-4.5 rounded-full flex items-center justify-center" style={{ background: "#1C2620cc" }}>
                    <X size={10} color={C.cream} />
                  </button>
                </div>
              ))}
              {editing.images.length < 5 && (
                <label className="w-16 h-20 rounded-sm border-2 border-dashed flex items-center justify-center cursor-pointer shrink-0" style={{ borderColor: "#1C262030" }}>
                  <Plus size={16} color="#8a8272" />
                  <input type="file" accept="image/*" multiple className="hidden" onChange={(e) => handleFiles(e.target.files)} />
                </label>
              )}
            </div>
          </div>

          <div className="flex gap-2 items-end">
            <div className="flex-1"><Input label="Nome da peça" value={editing.name} onChange={(v) => set("name", v)} /></div>
            <button onClick={() => genField("titulo")} disabled={aiLoading} className="btn-lift shrink-0 flex items-center gap-1 font-body text-[11px] px-3 py-2.5 rounded-full disabled:opacity-50" style={{ background: C.brass, color: C.ink }}>
              <Wand2 size={12} /> {aiLoading === "titulo" ? "..." : "IA"}
            </button>
          </div>

          <div className="grid grid-cols-2 gap-3">
            <Input label="Marca" value={editing.brand} onChange={(v) => set("brand", v)} />
            <Input label="Preço (R$)" value={editing.price} onChange={(v) => set("price", v.replace(/[^0-9.]/g, ""))} />
            <label className="block">
              <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>Categoria</span>
              <select value={editing.category} onChange={(e) => set("category", e.target.value)} className="w-full mt-1 font-body text-[13px] px-3 py-2.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }}>
                {CATEGORIES.map((c) => <option key={c}>{c}</option>)}
              </select>
            </label>
            <label className="block">
              <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>Gênero</span>
              <select value={editing.gender} onChange={(e) => set("gender", e.target.value)} className="w-full mt-1 font-body text-[13px] px-3 py-2.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }}>
                {GENDERS.map((c) => <option key={c}>{c}</option>)}
              </select>
            </label>
            <Input label="Cor" value={editing.color} onChange={(v) => set("color", v)} />
            <Input label="Tamanho" value={editing.size} onChange={(v) => set("size", v)} />
            <label className="block col-span-2">
              <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>Estado da peça</span>
              <select value={editing.condition} onChange={(e) => set("condition", e.target.value)} className="w-full mt-1 font-body text-[13px] px-3 py-2.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }}>
                {CONDITIONS.map((c) => <option key={c}>{c}</option>)}
              </select>
            </label>
          </div>

          <div>
            <div className="flex items-center justify-between">
              <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>Descrição</span>
              <button onClick={() => genField("descricao")} disabled={aiLoading} className="flex items-center gap-1 font-mono text-[10px] disabled:opacity-50" style={{ color: C.burgundy }}>
                <Wand2 size={11} /> {aiLoading === "descricao" ? "gerando..." : "gerar com IA"}
              </button>
            </div>
            <textarea value={editing.description} onChange={(e) => set("description", e.target.value)} rows={3} className="w-full mt-1 font-body text-[13px] px-3 py-2.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }} />
          </div>

          <label className="flex items-center gap-2">
            <input type="checkbox" checked={editing.featured} onChange={(e) => set("featured", e.target.checked)} />
            <span className="font-body text-[12px]" style={{ color: C.ink }}>Mostrar em destaque na home</span>
          </label>

          <div className="rounded-sm border p-3" style={{ borderColor: "#1C262018", background: C.parchment }}>
            <p className="font-body text-[11px] uppercase tracking-wide mb-2" style={{ color: "#5B5346" }}>Textos para divulgar (opcional)</p>
            <div className="flex gap-2 mb-2">
              <button onClick={() => genField("instagram")} disabled={aiLoading} className="flex items-center gap-1 font-body text-[11px] px-3 py-1.5 rounded-full disabled:opacity-50" style={{ background: C.ink, color: C.cream }}>
                <Sparkles size={11} /> Legenda Instagram
              </button>
              <button onClick={() => genField("whatsapp")} disabled={aiLoading} className="flex items-center gap-1 font-body text-[11px] px-3 py-1.5 rounded-full disabled:opacity-50" style={{ background: C.ink, color: C.cream }}>
                <Sparkles size={11} /> Texto WhatsApp
              </button>
            </div>
            {socialText && <p className="font-body text-[12px] whitespace-pre-wrap" style={{ color: C.ink }}>{socialText}</p>}
          </div>

          <button onClick={onSave} className="btn-lift w-full py-3 rounded-full font-body text-sm mt-1 shadow-sm" style={{ background: C.ink, color: C.cream }}>
            Salvar produto
          </button>
        </div>
      </div>
    </div>
  );
}

function AdminOrders({ orders }) {
  const demo = orders.length ? orders : [
    { id: "1042", email: "cliente@email.com", date: "01/07/2026", total: 189, status: "Pago", items: ["p1"] },
    { id: "1041", email: "maria@email.com", date: "30/06/2026", total: 264, status: "Enviado", items: ["p2", "p3"] },
  ];
  const [statusMap, setStatusMap] = useState({});
  return (
    <div>
      <h1 className="font-display text-2xl mb-6" style={{ color: C.ink }}>Pedidos</h1>
      <div className="rounded-sm border overflow-hidden" style={{ borderColor: "#1C262018", background: C.cream }}>
        {demo.map((o) => (
          <div key={o.id} className="flex items-center gap-3 px-4 py-3 border-b last:border-0 flex-wrap" style={{ borderColor: "#1C262012" }}>
            <span className="font-mono text-[12px]" style={{ color: C.ink }}>#{o.id}</span>
            <span className="font-body text-[12px] flex-1 min-w-[120px]" style={{ color: "#5B5346" }}>{o.email}</span>
            <span className="font-body text-[12px]" style={{ color: "#5B5346" }}>{o.date}</span>
            <span className="font-mono text-[12px] font-bold" style={{ color: C.ink }}>{brl(o.total)}</span>
            <select
              value={statusMap[o.id] || o.status}
              onChange={(e) => setStatusMap((s) => ({ ...s, [o.id]: e.target.value }))}
              className="font-body text-[11px] px-2.5 py-1.5 rounded-full border outline-none"
              style={{ borderColor: "#1C262030", background: C.parchment, color: C.ink }}
            >
              {["Aguardando pagamento", "Pago", "Em separação", "Enviado", "Entregue"].map((s) => <option key={s}>{s}</option>)}
            </select>
          </div>
        ))}
      </div>
    </div>
  );
}

function AdminCustomers({ orders }) {
  const emails = [...new Set(orders.map((o) => o.email))];
  const demo = emails.length ? emails : ["cliente@email.com", "maria@email.com", "joana@email.com"];
  return (
    <div>
      <h1 className="font-display text-2xl mb-6" style={{ color: C.ink }}>Clientes</h1>
      <div className="rounded-sm border overflow-hidden" style={{ borderColor: "#1C262018", background: C.cream }}>
        {demo.map((e) => (
          <div key={e} className="flex items-center gap-3 px-4 py-3 border-b last:border-0" style={{ borderColor: "#1C262012" }}>
            <div className="w-8 h-8 rounded-full flex items-center justify-center" style={{ background: C.parchment2 }}><User size={14} color={C.ink} /></div>
            <span className="font-body text-[13px]" style={{ color: C.ink }}>{e}</span>
          </div>
        ))}
      </div>
    </div>
  );
}

function AdminAI({ products }) {
  const [productName, setProductName] = useState(products[0]?.name || "");
  const [context, setContext] = useState("Vestido midi verde, alfaiataria, tamanho M, estado como novo, R$189");
  const [output, setOutput] = useState("");
  const [loading, setLoading] = useState(false);
  const [mode, setMode] = useState("titulo");

  const modes = {
    titulo: { label: "Título do produto", sys: "Você cria títulos curtos e vendáveis para peças de brechó, em português, no máximo 8 palavras." },
    descricao: { label: "Descrição do produto", sys: "Você escreve descrições de produto para um brechó de curadoria, tom sofisticado e caloroso, 2-3 frases, em português." },
    instagram: { label: "Legenda Instagram", sys: "Você escreve legendas de Instagram para um brechó chamado Brechó Dutra, tom próximo e estiloso, com 1-2 emojis e sugestão de hashtags, em português." },
    whatsapp: { label: "Texto WhatsApp", sys: "Você escreve mensagens curtas de WhatsApp para avisar clientes sobre uma peça nova ou disponível, tom simpático e direto, em português." },
    look: { label: "Sugestão de look", sys: "Você é um styling assistant de brechó. Sugira uma combinação de look usando a peça descrita, em português, formato de lista curta." },
  };

  const generate = async () => {
    setLoading(true);
    const prompt = `Peça: ${productName}. Detalhes: ${context}.`;
    const text = await askClaude(prompt, modes[mode].sys);
    setOutput(text);
    setLoading(false);
  };

  return (
    <div>
      <h1 className="font-display text-2xl mb-2 flex items-center gap-2" style={{ color: C.ink }}><Sparkles size={20} color={C.brass} /> IA para conteúdo</h1>
      <p className="font-body text-[13px] mb-6" style={{ color: "#5B5346" }}>Gere títulos, descrições, legendas e sugestões de look automaticamente.</p>

      <div className="grid md:grid-cols-2 gap-6">
        <div className="p-5 rounded-sm border" style={{ background: C.cream, borderColor: "#1C262018" }}>
          <div className="flex flex-wrap gap-2 mb-4">
            {Object.entries(modes).map(([k, v]) => (
              <button key={k} onClick={() => setMode(k)} className="px-3 py-1.5 rounded-full font-body text-[11px]" style={{ background: mode === k ? C.ink : "#1C262010", color: mode === k ? C.cream : C.ink }}>
                {v.label}
              </button>
            ))}
          </div>
          <div className="flex flex-col gap-3">
            <Input label="Produto" value={productName} onChange={setProductName} />
            <label className="block">
              <span className="font-body text-[11px] uppercase tracking-wide" style={{ color: "#5B5346" }}>Detalhes da peça</span>
              <textarea value={context} onChange={(e) => setContext(e.target.value)} rows={3} className="w-full mt-1 font-body text-[13px] px-3 py-2.5 rounded-sm border outline-none" style={{ borderColor: "#1C262030" }} />
            </label>
            <button onClick={generate} disabled={loading} className="w-full flex items-center justify-center gap-2 py-2.5 rounded-full font-body text-sm mt-1 disabled:opacity-60" style={{ background: C.brass, color: C.ink }}>
              <Wand2 size={14} /> {loading ? "Gerando..." : "Gerar com IA"}
            </button>
          </div>
        </div>

        <div className="p-5 rounded-sm border" style={{ background: C.cream, borderColor: "#1C262018" }}>
          <p className="font-body text-[12px] uppercase tracking-wide mb-3" style={{ color: "#5B5346" }}>Resultado</p>
          <div className="font-body text-[13px] whitespace-pre-wrap min-h-[160px]" style={{ color: C.ink }}>
            {output || "O texto gerado pela IA aparecerá aqui."}
          </div>
        </div>
      </div>
    </div>
  );
}

/* ------------------------------------------------------------------ */
/* CHAT WIDGET                                                          */
/* ------------------------------------------------------------------ */
function ChatWidget() {
  const [open, setOpen] = useState(false);
  const [messages, setMessages] = useState([
    { role: "bot", text: "Oi! Sou a assistente virtual do Brechó Dutra 🌿 Posso ajudar com dúvidas sobre peças, tamanhos, pagamento via Pix ou entregas." },
  ]);
  const [input, setInput] = useState("");
  const [loading, setLoading] = useState(false);
  const [handoff, setHandoff] = useState(false);
  const endRef = useRef(null);

  useEffect(() => { endRef.current?.scrollIntoView({ behavior: "smooth" }); }, [messages, open]);

  const send = async () => {
    if (!input.trim() || loading) return;
    const userMsg = input.trim();
    setMessages((m) => [...m, { role: "user", text: userMsg }]);
    setInput("");
    setLoading(true);
    const sys = `Você é a assistente virtual do Brechó Dutra, um brechó online. Responda dúvidas frequentes: peças são únicas (sem reposição de estoque), pagamento apenas via Pix, entrega combinada após a compra, trocas avaliadas caso a caso. Seja breve e simpática, em português. Se a pergunta não for sobre a loja ou você não souber responder com certeza, responda EXATAMENTE com: "TRANSFERIR_HUMANO" seguido de nada mais.`;
    const reply = await askClaude(userMsg, sys);
    if (reply.includes("TRANSFERIR_HUMANO")) {
      setHandoff(true);
      setMessages((m) => [...m, { role: "bot", text: "Não tenho certeza sobre isso — vou encaminhar sua pergunta para a Dutra, que responde em breve por aqui ou pelo WhatsApp." }]);
    } else {
      setMessages((m) => [...m, { role: "bot", text: reply }]);
    }
    setLoading(false);
  };

  return (
    <>
      <button
        onClick={() => setOpen(!open)}
        className="fixed bottom-5 right-5 z-40 w-14 h-14 rounded-full flex items-center justify-center shadow-lg"
        style={{ background: C.burgundy }}
        aria-label="Abrir chat"
      >
        {open ? <X size={22} color={C.cream} /> : <Bot size={22} color={C.cream} />}
      </button>

      {open && (
        <div className="fixed bottom-24 right-5 z-40 w-[90vw] max-w-sm h-[60vh] rounded-md flex flex-col overflow-hidden shadow-2xl" style={{ background: C.cream }}>
          <div className="px-4 py-3 flex items-center gap-2" style={{ background: C.ink }}>
            <Bot size={16} color={C.brass} />
            <p className="font-body text-[13px] font-medium" style={{ color: C.cream }}>Atendimento Brechó Dutra</p>
          </div>
          <div className="flex-1 overflow-y-auto p-4 flex flex-col gap-3 scrollbar-thin">
            {messages.map((m, i) => (
              <div key={i} className={`max-w-[85%] px-3 py-2 rounded-md font-body text-[13px] ${m.role === "user" ? "self-end" : "self-start"}`} style={{ background: m.role === "user" ? C.brass : C.parchment, color: C.ink }}>
                {m.text}
              </div>
            ))}
            {loading && <div className="font-body text-[12px]" style={{ color: "#5B5346" }}>digitando...</div>}
            {handoff && <div className="self-start font-mono text-[10px] px-2 py-1 rounded-full" style={{ background: C.burgundy, color: C.cream }}>encaminhado para a administradora</div>}
            <div ref={endRef} />
          </div>
          <div className="p-3 flex gap-2 border-t" style={{ borderColor: "#1C262018" }}>
            <input
              value={input}
              onChange={(e) => setInput(e.target.value)}
              onKeyDown={(e) => e.key === "Enter" && send()}
              placeholder="Digite sua dúvida..."
              className="flex-1 font-body text-[13px] px-3 py-2 rounded-full border outline-none"
              style={{ borderColor: "#1C262030" }}
            />
            <button onClick={send} className="w-9 h-9 rounded-full flex items-center justify-center shrink-0" style={{ background: C.ink }}>
              <Send size={14} color={C.cream} />
            </button>
          </div>
        </div>
      )}
    </>
  );
}

/* ------------------------------------------------------------------ */
/* APP ROOT                                                             */
/* ------------------------------------------------------------------ */
export default function BrechoDutra() {
  const [products, setProducts] = useState(seedProducts);
  const [orders, setOrders] = useState([]);
  const [route, setRoute] = useState("home");
  const [routeParams, setRouteParams] = useState({});
  const [selectedId, setSelectedId] = useState(null);
  const [cart, setCart] = useState([]);
  const [favorites, setFavorites] = useState(new Set());
  const [cartOpen, setCartOpen] = useState(false);
  const [checkoutOpen, setCheckoutOpen] = useState(false);
  const [authMode, setAuthMode] = useState(null);
  const [user, setUser] = useState(null);
  const [search, setSearch] = useState("");

  const nav = (r, params) => { setRoute(r); setRouteParams(params || {}); window.scrollTo(0, 0); };
  const openProduct = (id) => { setSelectedId(id); nav("product"); };

  const addCart = (id) => setCart((c) => (c.includes(id) ? c : [...c, id]));
  const removeFromCart = (id) => setCart((c) => c.filter((x) => x !== id));
  const buyNow = (id) => { addCart(id); setCartOpen(false); setCheckoutOpen(true); };
  const toggleFav = (id) => setFavorites((f) => { const n = new Set(f); n.has(id) ? n.delete(id) : n.add(id); return n; });

  const confirmPayment = () => {
    const boughtIds = [...cart];
    const total = boughtIds.reduce((s, id) => s + (products.find((p) => p.id === id)?.price || 0), 0);
    setOrders((o) => [...o, { id: String(1000 + o.length + 1), email: user?.email || "convidado@email.com", date: "01/07/2026", total, status: "Pago", items: boughtIds }]);
    setProducts((ps) => ps.filter((p) => !boughtIds.includes(p.id)));
    setCart([]);
  };

  const login = (u) => {
    const isAdmin = u.email.toLowerCase().includes("admin");
    setUser({ ...u, isAdmin, address: "" });
    setAuthMode(null);
    nav(isAdmin ? "admin" : "home");
  };
  const logout = () => setUser(null);

  const suggestions = useMemo(() => {
    const q = search.trim().toLowerCase();
    if (!q) return [];
    return products.filter((p) => [p.name, p.brand, p.category, p.color, p.size, p.description].join(" ").toLowerCase().includes(q));
  }, [search, products]);

  const selectedProduct = products.find((p) => p.id === selectedId);

  if (route === "admin" && user?.isAdmin) {
    return <AdminPanel products={products} orders={orders} logout={() => { logout(); nav("home"); }} />;
  }

  return (
    <div className="font-body min-h-screen grain" style={{ background: C.parchment }}>
      <FontStyle />
      <Header
        nav={nav}
        route={route}
        search={search}
        setSearch={setSearch}
        cartCount={cart.length}
        favCount={favorites.size}
        user={user}
        onCartOpen={() => setCartOpen(true)}
        onAuthOpen={setAuthMode}
        onAccount={() => nav("account")}
        suggestions={suggestions}
        onPickSuggestion={(id) => { if (id) openProduct(id); else nav("catalog"); }}
      />

      {route === "home" && <Home products={products} nav={nav} openProduct={openProduct} addCart={addCart} favorites={favorites} toggleFav={toggleFav} />}
      {route === "catalog" && <Catalog products={products} initialFilters={routeParams} openProduct={openProduct} addCart={addCart} favorites={favorites} toggleFav={toggleFav} search={search} setSearch={setSearch} />}
      {route === "product" && selectedProduct && (
        <ProductDetail product={selectedProduct} products={products} back={() => nav("catalog")} addCart={addCart} buyNow={buyNow} favorites={favorites} toggleFav={toggleFav} openProduct={openProduct} />
      )}
      {route === "favorites" && <FavoritesPage products={products} favorites={favorites} openProduct={openProduct} addCart={addCart} toggleFav={toggleFav} />}
      {route === "account" && (user ? <AccountPage user={user} orders={orders} favorites={favorites} products={products} logout={logout} nav={nav} /> : <div className="text-center py-24 font-body" style={{ color: C.ink }}>Faça login para ver sua conta.</div>)}

      <Footer nav={nav} />

      <CartDrawer
        open={cartOpen}
        close={() => setCartOpen(false)}
        items={cart}
        products={products}
        removeItem={removeFromCart}
        checkout={() => { setCartOpen(false); setCheckoutOpen(true); }}
      />
      <CheckoutModal
        open={checkoutOpen}
        close={() => setCheckoutOpen(false)}
        items={cart}
        products={products}
        confirmPayment={confirmPayment}
      />
      <AuthModal mode={authMode} setMode={setAuthMode} close={() => setAuthMode(null)} login={login} />

      <ChatWidget />
    </div>
  );
}
