import React, { useState, useMemo } from "react";
import {
  Users, Target, Package, ShoppingCart, Stethoscope, Wallet, BarChart3,
  MapPin, MessageCircle, LogOut, Plus, X, ChevronRight, Mail, Shield,
  TrendingUp, TrendingDown, Building2, Send, CheckCircle2
} from "lucide-react";
import {
  BarChart, Bar, XAxis, YAxis, CartesianGrid, Tooltip, ResponsiveContainer, Legend, PieChart, Pie, Cell
} from "recharts";

// ---- Design tokens ----
const C = {
  ink: "#0F1B2D",
  inkSoft: "#16263D",
  surface: "#FFFFFF",
  surfaceAlt: "#F2F6F6",
  line: "#DCE6E6",
  teal: "#1D7A6E",
  tealDark: "#14544C",
  tealPale: "#E4F1EE",
  amber: "#C9622D",
  amberPale: "#FBEBE1",
  success: "#2F9E44",
  danger: "#C0392B",
  text: "#152229",
  muted: "#5E7075",
};

const ROLES = [
  { key: "country", label: "Country Manager", icon: Shield, level: 0 },
  { key: "regional", label: "Regional Manager", icon: Building2, level: 1 },
  { key: "area", label: "Area Sales Manager", icon: MapPin, level: 2 },
  { key: "mr", label: "Marketing Representative", icon: Users, level: 3 },
];

// ---- Mock data (Pharmamandu Dot Com Pvt. Ltd.) ----
const initialUsers = [
  { id: "u1", name: "Deepak Kumar Pant", role: "country", region: "Nepal", area: "-", manager: "-", target: { monthly: 1200000, quarterly: 3600000, yearly: 14400000 }, achieved: { monthly: 940000, quarterly: 2650000, yearly: 9300000 }, email: "deepak.pant@pharmamandu.com" },
  { id: "u2", name: "Niyati Pathak", role: "mr", region: "Bagmati", area: "Kathmandu Valley", manager: "Deepak Kumar Pant", target: { monthly: 650000, quarterly: 1950000, yearly: 7800000 }, achieved: { monthly: 520000, quarterly: 1480000, yearly: 5100000 }, email: "niyati.pathak@pharmamandu.com" },
  { id: "u3", name: "Rishav Neupane", role: "mr", region: "Bagmati", area: "Kathmandu Valley", manager: "Deepak Kumar Pant", target: { monthly: 550000, quarterly: 1650000, yearly: 6600000 }, achieved: { monthly: 420000, quarterly: 1170000, yearly: 4200000 }, email: "rishav.neupane@pharmamandu.com" },
];

const initialProducts = [
  { id: "p1", name: "Cap. Cyto-Min", division: "Oncology Nutraceutical" },
  { id: "p2", name: "Cap. Cyto-12", division: "Oncology Nutraceutical" },
  { id: "p3", name: "Tab. Cyto-Cal", division: "Oncology Support" },
  { id: "p4", name: "Tab. Multiplat", division: "Oncology" },
  { id: "p5", name: "Protein. Cyto.Pro", division: "Nutraceutical" },
  { id: "p6", name: "Radiosoothe Ointment", division: "Dermatology / Onco-support" },
  { id: "p7", name: "Radiosoothe Oro Spray", division: "Dermatology / Onco-support" },
];

const initialHospitals = [
  { id: "h1", name: "Nepal Cancer Hospital" },
  { id: "h2", name: "Ohm Hospital" },
  { id: "h3", name: "Bhaktapur Cancer Hospital" },
  { id: "h4", name: "Neorvic Hospital" },
  { id: "h5", name: "Helios Hospital" },
  { id: "h6", name: "National Cancer Hospital" },
];

const initialDoctors = [
  { id: "d1", name: "Dr. Sudip Shrestha", hospital: "Nepal Cancer Hospital", mrId: "u2", sales: [{ productId: "p1", value: 38000, month: "2026-07" }] },
  { id: "d2", name: "Dr. Roshan Prajapati", hospital: "Ohm Hospital", mrId: "u2", sales: [{ productId: "p2", value: 29000, month: "2026-07" }] },
  { id: "d3", name: "Dr. Arun Shahi", hospital: "Bhaktapur Cancer Hospital", mrId: "u3", sales: [{ productId: "p4", value: 51000, month: "2026-07" }] },
  { id: "d4", name: "Dr. Anuj KC", hospital: "Neorvic Hospital", mrId: "u3", sales: [{ productId: "p5", value: 22000, month: "2026-07" }] },
  { id: "d5", name: "Dr. Sudip Thapa", hospital: "Helios Hospital", mrId: "u2", sales: [{ productId: "p3", value: 33000, month: "2026-07" }] },
  { id: "d6", name: "Dr. R.P. Baral", hospital: "National Cancer Hospital", mrId: "u3", sales: [{ productId: "p1", value: 46000, month: "2026-07" }] },
  { id: "d7", name: "Dr. Sweta Baral", hospital: "Nepal Cancer Hospital", mrId: "u2", sales: [{ productId: "p6", value: 15000, month: "2026-07" }] },
  { id: "d8", name: "Dr. Sachin Shakya", hospital: "Ohm Hospital", mrId: "u3", sales: [{ productId: "p2", value: 27000, month: "2026-07" }] },
  { id: "d9", name: "Dr. Bishal Poudel", hospital: "Bhaktapur Cancer Hospital", mrId: "u2", sales: [{ productId: "p7", value: 12000, month: "2026-07" }] },
  { id: "d10", name: "Dr. Niraj Singh", hospital: "Helios Hospital", mrId: "u3", sales: [{ productId: "p3", value: 19000, month: "2026-07" }] },
  { id: "d11", name: "Dr. Reetu Lamichhane", hospital: "National Cancer Hospital", mrId: "u2", sales: [{ productId: "p4", value: 41000, month: "2026-07" }] },
];

const initialOrders = [
  { id: "o1", mrId: "u2", product: "Cap. Cyto-Min", qty: 120, destination: "Company - Direct", status: "Dispatched", date: "2026-07-21" },
  { id: "o2", mrId: "u3", product: "Tab. Multiplat", qty: 80, destination: "Stockist - Everest Pharma Distributors", status: "Pending", date: "2026-07-24" },
];

const initialCash = [
  { id: "c1", mrId: "u2", amount: 62000, note: "Kathmandu valley round collection", date: "2026-07-22" },
  { id: "c2", mrId: "u3", amount: 48500, note: "Bhaktapur - Nepal Cancer Hospital area", date: "2026-07-23" },
];

const initialLocations = [
  { mrId: "u2", area: "Nepal Cancer Hospital, Kathmandu", lastSeen: "2 min ago", status: "At doctor visit" },
  { mrId: "u3", area: "Bhaktapur Cancer Hospital", lastSeen: "just now", status: "On field visit" },
];

const initialVisits = [
  { id: "v1", mrId: "u2", date: "2026-07-24", doctorId: "d1", hospital: "Nepal Cancer Hospital", notes: "Discussed Cyto-Min dosing update, sample left." },
  { id: "v2", mrId: "u3", date: "2026-07-24", doctorId: "d3", hospital: "Bhaktapur Cancer Hospital", notes: "Follow-up on Tab. Multiplat trial patients." },
  { id: "v3", mrId: "u2", date: "2026-07-23", doctorId: "d7", hospital: "Nepal Cancer Hospital", notes: "Introduced Radiosoothe Ointment." },
];

function fmtNPR(n) {
  return "Rs " + Number(n || 0).toLocaleString("en-IN");
}

function pct(a, b) {
  if (!b) return 0;
  return Math.round((a / b) * 100);
}

// ---- Small UI atoms ----
function Badge({ children, tone = "teal" }) {
  const tones = {
    teal: { bg: C.tealPale, fg: C.tealDark },
    amber: { bg: C.amberPale, fg: C.amber },
    success: { bg: "#E6F6E9", fg: C.success },
    danger: { bg: "#FBEAE8", fg: C.danger },
  };
  const t = tones[tone];
  return (
    <span style={{ background: t.bg, color: t.fg }} className="px-2 py-0.5 rounded text-xs font-mono font-semibold tracking-wide">
      {children}
    </span>
  );
}

function ProgressBar({ value, tone = "teal" }) {
  const color = value >= 100 ? C.success : value >= 70 ? C.teal : C.amber;
  return (
    <div style={{ background: C.line }} className="w-full h-2 rounded-full overflow-hidden">
      <div style={{ width: Math.min(value, 100) + "%", background: color }} className="h-full rounded-full transition-all" />
    </div>
  );
}

function Card({ children, className = "", style = {} }) {
  return (
    <div style={{ background: C.surface, border: `1px solid ${C.line}`, ...style }} className={`rounded-xl p-5 ${className}`}>
      {children}
    </div>
  );
}

function SectionLabel({ eyebrow, title }) {
  return (
    <div className="mb-4">
      <div style={{ color: C.teal }} className="text-xs font-mono font-semibold tracking-[0.15em] uppercase mb-1">{eyebrow}</div>
      <h2 style={{ color: C.ink }} className="text-xl font-bold">{title}</h2>
    </div>
  );
}

// ---- Login ----
function Login({ onLogin }) {
  const [step, setStep] = useState("role"); // role -> email -> otp
  const [role, setRole] = useState(null);
  const [email, setEmail] = useState("");
  const [otp, setOtp] = useState("");
  const [sentOtp, setSentOtp] = useState("");

  const sendOtp = () => {
    const code = String(Math.floor(100000 + Math.random() * 900000));
    setSentOtp(code);
    setStep("otp");
  };

  return (
    <div style={{ background: C.ink }} className="min-h-screen flex items-center justify-center p-6">
      <div style={{ background: C.surface }} className="w-full max-w-md rounded-2xl p-8 shadow-2xl">
        <div className="flex items-center gap-2 mb-1">
          <div style={{ background: C.teal }} className="w-9 h-9 rounded-lg flex items-center justify-center">
            <Package size={18} color="#fff" />
          </div>
          <span style={{ color: C.ink }} className="font-bold text-lg tracking-tight">Pharmamandu</span>
        </div>
        <p style={{ color: C.muted }} className="text-sm mb-6 font-mono">Field Sales &amp; Distribution Console</p>

        {step === "role" && (
          <>
            <div style={{ color: C.muted }} className="text-xs font-mono uppercase tracking-wider mb-3">Sign in as</div>
            <div className="grid grid-cols-1 gap-2">
              {ROLES.map((r) => {
                const Icon = r.icon;
                return (
                  <button
                    key={r.key}
                    onClick={() => { setRole(r.key); setStep("email"); }}
                    style={{ borderColor: C.line }}
                    className="flex items-center gap-3 border rounded-lg px-4 py-3 hover:border-current text-left transition-colors"
                  >
                    <Icon size={18} color={C.teal} />
                    <span style={{ color: C.text }} className="font-medium text-sm">{r.label}</span>
                    <ChevronRight size={16} className="ml-auto" color={C.muted} />
                  </button>
                );
              })}
            </div>
            <div className="flex items-center gap-2 my-4">
              <div style={{ background: C.line }} className="h-px flex-1" />
              <span style={{ color: C.muted }} className="text-[10px] font-mono uppercase">or</span>
              <div style={{ background: C.line }} className="h-px flex-1" />
            </div>
            <button
              onClick={() => setStep("guestRole")}
              style={{ borderColor: C.line, color: C.muted }}
              className="w-full border rounded-lg px-4 py-2.5 text-sm font-medium hover:border-current"
            >
              Continue as Guest (view-only demo)
            </button>
          </>
        )}

        {step === "guestRole" && (
          <>
            <div style={{ color: C.muted }} className="text-xs font-mono uppercase tracking-wider mb-3">Preview console as</div>
            <div className="grid grid-cols-1 gap-2 mb-3">
              {ROLES.map((r) => {
                const Icon = r.icon;
                return (
                  <button
                    key={r.key}
                    onClick={() => onLogin(r.key, "guest@pharmamandu.com", true)}
                    style={{ borderColor: C.line }}
                    className="flex items-center gap-3 border rounded-lg px-4 py-3 hover:border-current text-left transition-colors"
                  >
                    <Icon size={18} color={C.teal} />
                    <span style={{ color: C.text }} className="font-medium text-sm">{r.label}</span>
                    <ChevronRight size={16} className="ml-auto" color={C.muted} />
                  </button>
                );
              })}
            </div>
            <button onClick={() => setStep("role")} style={{ color: C.muted }} className="text-xs font-mono underline">
              ← back to sign in
            </button>
          </>
        )}

        {step === "email" && (
          <>
            <div style={{ color: C.muted }} className="text-xs font-mono uppercase tracking-wider mb-3">Verify your Gmail</div>
            <div className="flex items-center gap-2 border rounded-lg px-3 py-2 mb-3" style={{ borderColor: C.line }}>
              <Mail size={16} color={C.muted} />
              <input
                value={email}
                onChange={(e) => setEmail(e.target.value)}
                placeholder="name@gmail.com"
                className="w-full outline-none text-sm"
                style={{ color: C.text }}
              />
            </div>
            <button
              disabled={!email.includes("@")}
              onClick={sendOtp}
              style={{ background: C.teal }}
              className="w-full text-white text-sm font-semibold py-2.5 rounded-lg disabled:opacity-40"
            >
              Send verification code
            </button>
          </>
        )}

        {step === "otp" && (
          <>
            <div style={{ color: C.muted }} className="text-xs font-mono uppercase tracking-wider mb-2">Enter 6-digit code</div>
            <div style={{ background: C.tealPale, color: C.tealDark }} className="text-xs rounded-lg px-3 py-2 mb-3 font-mono">
              Demo mode — your code is <b>{sentOtp}</b> (in production this is emailed to {email})
            </div>
            <input
              value={otp}
              onChange={(e) => setOtp(e.target.value)}
              placeholder="••••••"
              maxLength={6}
              className="w-full border rounded-lg px-3 py-2 mb-3 text-sm tracking-[0.5em] font-mono text-center"
              style={{ borderColor: C.line, color: C.text }}
            />
            <button
              disabled={otp !== sentOtp}
              onClick={() => onLogin(role, email)}
              style={{ background: C.teal }}
              className="w-full text-white text-sm font-semibold py-2.5 rounded-lg disabled:opacity-40 flex items-center justify-center gap-2"
            >
              <CheckCircle2 size={16} /> Verify &amp; Enter Console
            </button>
          </>
        )}
      </div>
    </div>
  );
}

// ---- Chatbot ----
function Chatbot() {
  const [open, setOpen] = useState(false);
  const [msgs, setMsgs] = useState([
    { from: "bot", text: "Namaste! I'm the Pharmamandu assistant. Ask me about your target, orders, or how to log a doctor visit." },
  ]);
  const [input, setInput] = useState("");

  const reply = (text) => {
    const t = text.toLowerCase();
    if (t.includes("target")) return "Your monthly target and achievement are shown on your Dashboard tab, with quarterly and yearly roll-ups.";
    if (t.includes("order")) return "Go to Orders → New Order to place a request to the company or a stockist. Your manager gets notified automatically.";
    if (t.includes("doctor")) return "Use the Doctors tab to add a doctor and log product-wise sales value against their name.";
    if (t.includes("cash") || t.includes("collection")) return "Log collected cash under Cash Collection with amount, date, and a short note.";
    return "I can help with targets, orders, doctor logs, and cash collection. Try asking about one of those.";
  };

  const send = () => {
    if (!input.trim()) return;
    const userMsg = { from: "user", text: input };
    const botMsg = { from: "bot", text: reply(input) };
    setMsgs((m) => [...m, userMsg, botMsg]);
    setInput("");
  };

  return (
    <div className="fixed bottom-5 right-5 z-50">
      {open && (
        <div style={{ background: C.surface, border: `1px solid ${C.line}` }} className="w-80 h-96 rounded-xl shadow-2xl mb-3 flex flex-col overflow-hidden">
          <div style={{ background: C.ink }} className="px-4 py-3 flex items-center justify-between">
            <span className="text-white text-sm font-semibold">Pharmamandu Assistant</span>
            <button onClick={() => setOpen(false)}><X size={16} color="#fff" /></button>
          </div>
          <div className="flex-1 overflow-y-auto p-3 space-y-2">
            {msgs.map((m, i) => (
              <div key={i} className={`text-sm max-w-[85%] px-3 py-2 rounded-lg ${m.from === "bot" ? "" : "ml-auto text-white"}`}
                style={{ background: m.from === "bot" ? C.surfaceAlt : C.teal, color: m.from === "bot" ? C.text : "#fff" }}>
                {m.text}
              </div>
            ))}
          </div>
          <div className="p-2 border-t flex gap-2" style={{ borderColor: C.line }}>
            <input
              value={input}
              onChange={(e) => setInput(e.target.value)}
              onKeyDown={(e) => e.key === "Enter" && send()}
              placeholder="Ask something..."
              className="flex-1 text-sm px-3 py-2 rounded-lg outline-none"
              style={{ background: C.surfaceAlt, color: C.text }}
            />
            <button onClick={send} style={{ background: C.teal }} className="p-2 rounded-lg"><Send size={14} color="#fff" /></button>
          </div>
        </div>
      )}
      <button
        onClick={() => setOpen((o) => !o)}
        style={{ background: C.teal }}
        className="w-12 h-12 rounded-full shadow-xl flex items-center justify-center"
      >
        <MessageCircle size={22} color="#fff" />
      </button>
    </div>
  );
}

// ---- Main App ----
export default function App() {
  const [session, setSession] = useState(null); // {role, email}
  const [tab, setTab] = useState("dashboard");
  const [period, setPeriod] = useState("monthly");

  const [users, setUsers] = useState(initialUsers);
  const [products, setProducts] = useState(initialProducts);
  const [doctors, setDoctors] = useState(initialDoctors);
  const [orders, setOrders] = useState(initialOrders);
  const [cash, setCash] = useState(initialCash);
  const [locations] = useState(initialLocations);
  const [hospitals, setHospitals] = useState(initialHospitals);
  const [visits, setVisits] = useState(initialVisits);

  const [showAddUser, setShowAddUser] = useState(false);
  const [showAddProduct, setShowAddProduct] = useState(false);
  const [showAddDoctor, setShowAddDoctor] = useState(false);
  const [showAddOrder, setShowAddOrder] = useState(false);
  const [showAddCash, setShowAddCash] = useState(false);
  const [showAddHospital, setShowAddHospital] = useState(false);
  const [showAddPrescriber, setShowAddPrescriber] = useState(false);
  const [showAddVisit, setShowAddVisit] = useState(false);
  const [visitFilterMr, setVisitFilterMr] = useState("all");

  const currentUser = useMemo(() => {
    if (!session) return null;
    return users.find((u) => u.role === session.role) || users[0];
  }, [session, users]);

  const visibleUsers = useMemo(() => {
    if (!session) return [];
    if (session.role === "country") return users;
    if (session.role === "regional") return users.filter((u) => u.region === currentUser?.region || u.manager === currentUser?.name);
    if (session.role === "area") return users.filter((u) => u.manager === currentUser?.name || u.id === currentUser?.id);
    return users.filter((u) => u.id === currentUser?.id);
  }, [session, users, currentUser]);

  const mrList = users.filter((u) => u.role === "mr");

  const barData = mrList.map((u) => ({
    name: u.name.split(" ")[0],
    Target: u.target[period],
    Achieved: u.achieved[period],
  }));

  const divisionData = useMemo(() => {
    const map = {};
    products.forEach((p) => { map[p.division] = (map[p.division] || 0) + 1; });
    return Object.entries(map).map(([name, value]) => ({ name, value }));
  }, [products]);

  const pieColors = [C.teal, C.amber, C.tealDark, C.success, "#7A8FA0"];

  if (!session) return <Login onLogin={(role, email, guest) => setSession({ role, email, guest: !!guest })} />;

  const roleInfo = ROLES.find((r) => r.key === session.role);

  const NAV = [
    { key: "dashboard", label: "Dashboard", icon: BarChart3 },
    { key: "hierarchy", label: "Team & Hierarchy", icon: Users },
    { key: "targets", label: "Targets", icon: Target },
    { key: "products", label: "Master Data", icon: Package },
    { key: "orders", label: "Orders", icon: ShoppingCart },
    { key: "doctors", label: "Doctors & Sales", icon: Stethoscope },
    { key: "cash", label: "Cash Collection", icon: Wallet },
    { key: "comparison", label: "MR Comparison", icon: TrendingUp },
    { key: "location", label: "Location Tracking", icon: MapPin },
    { key: "visits", label: "Daily Visits", icon: CheckCircle2 },
  ];

  return (
    <div style={{ background: C.surfaceAlt, minHeight: "100vh", color: C.text }} className="flex font-sans text-sm">
      {/* Sidebar */}
      <div style={{ background: C.ink, width: 240 }} className="flex-shrink-0 flex flex-col py-5 px-3 min-h-screen">
        <div className="flex items-center gap-2 px-2 mb-6">
          <div style={{ background: C.teal }} className="w-8 h-8 rounded-lg flex items-center justify-center">
            <Package size={16} color="#fff" />
          </div>
          <div>
            <div className="text-white font-bold text-sm leading-tight">Pharmamandu</div>
            <div style={{ color: "#7A8FA0" }} className="text-[10px] font-mono">Sales Console</div>
          </div>
        </div>
        <div className="flex flex-col gap-0.5">
          {NAV.map((n) => {
            const Icon = n.icon;
            const active = tab === n.key;
            return (
              <button
                key={n.key}
                onClick={() => setTab(n.key)}
                style={{ background: active ? C.teal : "transparent", color: active ? "#fff" : "#B7C4CC" }}
                className="flex items-center gap-2.5 px-3 py-2 rounded-lg text-left text-[13px] font-medium transition-colors"
              >
                <Icon size={15} />
                {n.label}
              </button>
            );
          })}
        </div>
        <div className="mt-auto px-2">
          <div style={{ borderColor: "#22344A" }} className="border-t pt-3 mt-3 flex items-center justify-between">
            <div>
              <div className="text-white text-xs font-semibold flex items-center gap-1.5">
                {session.guest ? "Guest Preview" : currentUser?.name}
                {session.guest && <span style={{ background: C.amber }} className="text-[9px] px-1.5 py-0.5 rounded font-mono">VIEW-ONLY</span>}
              </div>
              <div style={{ color: "#7A8FA0" }} className="text-[10px] font-mono">{roleInfo.label}</div>
            </div>
            <button onClick={() => setSession(null)} title="Log out">
              <LogOut size={15} color="#B7C4CC" />
            </button>
          </div>
        </div>
      </div>

      {/* Main */}
      <div className="flex-1 p-8 overflow-y-auto max-h-screen">
        {tab === "dashboard" && (
          <div>
            <SectionLabel eyebrow={`${roleInfo.label} · Overview`} title={`Welcome, ${currentUser?.name.split(" ")[0]}`} />
            <div className="grid grid-cols-3 gap-4 mb-6">
              {["monthly", "quarterly", "yearly"].map((p) => (
                <Card key={p}>
                  <div style={{ color: C.muted }} className="text-xs font-mono uppercase tracking-wide mb-2">{p} target</div>
                  <div style={{ color: C.ink }} className="text-2xl font-bold mb-1">{fmtNPR(currentUser?.achieved[p])}</div>
                  <div style={{ color: C.muted }} className="text-xs mb-3">of {fmtNPR(currentUser?.target[p])} target</div>
                  <ProgressBar value={pct(currentUser?.achieved[p], currentUser?.target[p])} />
                  <div className="flex items-center gap-1 mt-2">
                    <Badge tone={pct(currentUser?.achieved[p], currentUser?.target[p]) >= 100 ? "success" : "amber"}>
                      {pct(currentUser?.achieved[p], currentUser?.target[p])}% achieved
                    </Badge>
                  </div>
                </Card>
              ))}
            </div>

            <Card className="mb-6">
              <div style={{ color: C.ink }} className="font-semibold mb-4">Reporting hierarchy roll-up</div>
              <div className="flex items-stretch gap-3 overflow-x-auto pb-2">
                {ROLES.map((r, i) => {
                  const roleUsers = users.filter((u) => u.role === r.key);
                  const totalTarget = roleUsers.reduce((s, u) => s + u.target.monthly, 0);
                  const totalAchieved = roleUsers.reduce((s, u) => s + u.achieved.monthly, 0);
                  const Icon = r.icon;
                  return (
                    <React.Fragment key={r.key}>
                      <div style={{ background: C.surfaceAlt, minWidth: 170 }} className="rounded-lg p-3 flex-shrink-0">
                        <div className="flex items-center gap-1.5 mb-2">
                          <Icon size={14} color={C.teal} />
                          <span style={{ color: C.ink }} className="text-xs font-semibold">{r.label}</span>
                        </div>
                        <div style={{ color: C.muted }} className="text-[10px] font-mono mb-1">{roleUsers.length} active</div>
                        <div style={{ color: C.ink }} className="text-sm font-mono font-bold">{fmtNPR(totalAchieved)}</div>
                        <div style={{ color: C.muted }} className="text-[10px] font-mono">/ {fmtNPR(totalTarget)}</div>
                        <div className="mt-2"><ProgressBar value={pct(totalAchieved, totalTarget)} /></div>
                      </div>
                      {i < ROLES.length - 1 && <ChevronRight className="self-center flex-shrink-0" size={16} color={C.muted} />}
                    </React.Fragment>
                  );
                })}
              </div>
            </Card>

            <Card>
              <div style={{ color: C.ink }} className="font-semibold mb-4">Sales vs target by MR — this month</div>
              <ResponsiveContainer width="100%" height={260}>
                <BarChart data={mrList.map((u) => ({ name: u.name.split(" ")[0], Target: u.target.monthly, Achieved: u.achieved.monthly }))}>
                  <CartesianGrid strokeDasharray="3 3" stroke={C.line} />
                  <XAxis dataKey="name" tick={{ fontSize: 11, fill: C.muted }} />
                  <YAxis tick={{ fontSize: 10, fill: C.muted }} tickFormatter={(v) => (v / 1000) + "k"} />
                  <Tooltip formatter={(v) => fmtNPR(v)} />
                  <Legend />
                  <Bar dataKey="Target" fill={C.line} radius={[4, 4, 0, 0]} />
                  <Bar dataKey="Achieved" fill={C.teal} radius={[4, 4, 0, 0]} />
                </BarChart>
              </ResponsiveContainer>
            </Card>
          </div>
        )}

        {tab === "hierarchy" && (
          <div>
            <div className="flex items-center justify-between">
              <SectionLabel eyebrow="Admin Panel" title="Team & Hierarchy" />
              <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddUser(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="h-fit text-white text-xs font-semibold px-3 py-2 rounded-lg flex items-center gap-1.5 disabled:cursor-not-allowed">
                <Plus size={14} /> Add Profile
              </button>
            </div>
            <Card>
              <table className="w-full text-left text-sm">
                <thead>
                  <tr style={{ color: C.muted }} className="text-xs font-mono uppercase border-b" style={{ borderColor: C.line }}>
                    <th className="py-2 pr-2">Name</th>
                    <th className="py-2 pr-2">Role</th>
                    <th className="py-2 pr-2">Region / Area</th>
                    <th className="py-2 pr-2">Reports to</th>
                    <th className="py-2 pr-2">Email</th>
                  </tr>
                </thead>
                <tbody>
                  {visibleUsers.map((u) => (
                    <tr key={u.id} className="border-b" style={{ borderColor: C.line }}>
                      <td className="py-2 pr-2 font-medium">{u.name}</td>
                      <td className="py-2 pr-2"><Badge>{ROLES.find((r) => r.key === u.role)?.label}</Badge></td>
                      <td className="py-2 pr-2" style={{ color: C.muted }}>{u.region} {u.area !== "-" ? "· " + u.area : ""}</td>
                      <td className="py-2 pr-2" style={{ color: C.muted }}>{u.manager}</td>
                      <td className="py-2 pr-2 font-mono text-xs" style={{ color: C.muted }}>{u.email}</td>
                    </tr>
                  ))}
                </tbody>
              </table>
            </Card>

            {showAddUser && (
              <Modal title="Add profile" onClose={() => setShowAddUser(false)}>
                <AddUserForm
                  users={users}
                  onAdd={(u) => { setUsers((arr) => [...arr, u]); setShowAddUser(false); }}
                  onCancel={() => setShowAddUser(false)}
                />
              </Modal>
            )}
          </div>
        )}

        {tab === "targets" && (
          <div>
            <SectionLabel eyebrow="Admin Panel" title="Sales Targets" />
            <Card>
              <table className="w-full text-left text-sm">
                <thead>
                  <tr style={{ color: C.muted }} className="text-xs font-mono uppercase border-b" style={{ borderColor: C.line }}>
                    <th className="py-2 pr-2">Name</th>
                    <th className="py-2 pr-2">Role</th>
                    <th className="py-2 pr-2">Monthly</th>
                    <th className="py-2 pr-2">Quarterly</th>
                    <th className="py-2 pr-2">Yearly</th>
                    <th className="py-2 pr-2">Achieved (M)</th>
                  </tr>
                </thead>
                <tbody>
                  {visibleUsers.map((u) => (
                    <tr key={u.id} className="border-b" style={{ borderColor: C.line }}>
                      <td className="py-2 pr-2 font-medium">{u.name}</td>
                      <td className="py-2 pr-2"><Badge>{ROLES.find((r) => r.key === u.role)?.label}</Badge></td>
                      <td className="py-2 pr-2 font-mono">
                        <input
                          type="number"
                          defaultValue={u.target.monthly}
                          onBlur={(e) => setUsers((arr) => arr.map((x) => x.id === u.id ? { ...x, target: { ...x.target, monthly: Number(e.target.value) } } : x))}
                          className="w-24 px-1 py-0.5 rounded border text-xs"
                          style={{ borderColor: C.line }}
                        />
                      </td>
                      <td className="py-2 pr-2 font-mono">{fmtNPR(u.target.quarterly)}</td>
                      <td className="py-2 pr-2 font-mono">{fmtNPR(u.target.yearly)}</td>
                      <td className="py-2 pr-2">
                        <Badge tone={pct(u.achieved.monthly, u.target.monthly) >= 100 ? "success" : "amber"}>{pct(u.achieved.monthly, u.target.monthly)}%</Badge>
                      </td>
                    </tr>
                  ))}
                </tbody>
              </table>
              <div style={{ color: C.muted }} className="text-xs font-mono mt-3">Click into a monthly target cell to edit inline. Quarterly / yearly recalculation would be handled server-side in production.</div>
            </Card>
          </div>
        )}

        {tab === "products" && (
          <div>
            <SectionLabel eyebrow="Admin Panel" title="Master Data" />
            <div style={{ color: C.muted }} className="text-xs font-mono mb-4 -mt-2">Edit the company's products, hospitals to visit, and prescriber roster here — MRs pick from these lists everywhere else in the console.</div>

            <div className="grid grid-cols-2 gap-4 mb-4">
              <Card>
                <div className="flex items-center justify-between mb-3">
                  <div style={{ color: C.ink }} className="font-semibold">Product catalog</div>
                  <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddProduct(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="text-white text-xs font-semibold px-2.5 py-1.5 rounded-lg flex items-center gap-1 disabled:cursor-not-allowed">
                    <Plus size={13} /> Add
                  </button>
                </div>
                <div className="space-y-2">
                  {products.map((p) => (
                    <div key={p.id} className="flex items-center justify-between py-2 border-b" style={{ borderColor: C.line }}>
                      <div>
                        <div className="font-medium">{p.name}</div>
                        <Badge tone="amber">{p.division}</Badge>
                      </div>
                      {!session.guest && (
                        <button onClick={() => setProducts((arr) => arr.filter((x) => x.id !== p.id))}>
                          <X size={14} color={C.muted} />
                        </button>
                      )}
                    </div>
                  ))}
                </div>
              </Card>

              <Card>
                <div style={{ color: C.ink }} className="font-semibold mb-3">Products per division</div>
                <ResponsiveContainer width="100%" height={220}>
                  <PieChart>
                    <Pie data={divisionData} dataKey="value" nameKey="name" outerRadius={80} label={(e) => e.name}>
                      {divisionData.map((_, i) => <Cell key={i} fill={pieColors[i % pieColors.length]} />)}
                    </Pie>
                    <Tooltip />
                  </PieChart>
                </ResponsiveContainer>
              </Card>
            </div>

            <div className="grid grid-cols-2 gap-4">
              <Card>
                <div className="flex items-center justify-between mb-3">
                  <div style={{ color: C.ink }} className="font-semibold">Hospitals to visit</div>
                  <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddHospital(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="text-white text-xs font-semibold px-2.5 py-1.5 rounded-lg flex items-center gap-1 disabled:cursor-not-allowed">
                    <Plus size={13} /> Add
                  </button>
                </div>
                <div className="space-y-2">
                  {hospitals.map((h) => (
                    <div key={h.id} className="flex items-center justify-between py-2 border-b" style={{ borderColor: C.line }}>
                      <span className="font-medium">{h.name}</span>
                      {!session.guest && (
                        <button onClick={() => setHospitals((arr) => arr.filter((x) => x.id !== h.id))}>
                          <X size={14} color={C.muted} />
                        </button>
                      )}
                    </div>
                  ))}
                </div>
              </Card>

              <Card>
                <div className="flex items-center justify-between mb-3">
                  <div style={{ color: C.ink }} className="font-semibold">Prescriber roster</div>
                  <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddPrescriber(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="text-white text-xs font-semibold px-2.5 py-1.5 rounded-lg flex items-center gap-1 disabled:cursor-not-allowed">
                    <Plus size={13} /> Add
                  </button>
                </div>
                <div className="space-y-2 max-h-72 overflow-y-auto">
                  {doctors.map((d) => (
                    <div key={d.id} className="flex items-center justify-between py-2 border-b" style={{ borderColor: C.line }}>
                      <div>
                        <div className="font-medium">{d.name}</div>
                        <div style={{ color: C.muted }} className="text-xs">{d.hospital} · {users.find((u) => u.id === d.mrId)?.name}</div>
                      </div>
                      {!session.guest && (
                        <button onClick={() => setDoctors((arr) => arr.filter((x) => x.id !== d.id))}>
                          <X size={14} color={C.muted} />
                        </button>
                      )}
                    </div>
                  ))}
                </div>
              </Card>
            </div>

            {showAddProduct && (
              <Modal title="Add product" onClose={() => setShowAddProduct(false)}>
                <AddProductForm onAdd={(p) => { setProducts((arr) => [...arr, p]); setShowAddProduct(false); }} onCancel={() => setShowAddProduct(false)} />
              </Modal>
            )}
            {showAddHospital && (
              <Modal title="Add hospital" onClose={() => setShowAddHospital(false)}>
                <AddHospitalForm onAdd={(h) => { setHospitals((arr) => [...arr, h]); setShowAddHospital(false); }} onCancel={() => setShowAddHospital(false)} />
              </Modal>
            )}
            {showAddPrescriber && (
              <Modal title="Add prescriber" onClose={() => setShowAddPrescriber(false)}>
                <AddPrescriberForm
                  mrList={mrList}
                  hospitals={hospitals}
                  onAdd={(d) => { setDoctors((arr) => [...arr, d]); setShowAddPrescriber(false); }}
                  onCancel={() => setShowAddPrescriber(false)}
                />
              </Modal>
            )}
          </div>
        )}

        {tab === "orders" && (
          <div>
            <div className="flex items-center justify-between">
              <SectionLabel eyebrow="Field Operations" title="Orders — Company & Stockist" />
              <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddOrder(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="h-fit text-white text-xs font-semibold px-3 py-2 rounded-lg flex items-center gap-1.5 disabled:cursor-not-allowed">
                <Plus size={14} /> New Order
              </button>
            </div>
            <Card>
              <table className="w-full text-left text-sm">
                <thead>
                  <tr style={{ color: C.muted }} className="text-xs font-mono uppercase border-b" style={{ borderColor: C.line }}>
                    <th className="py-2 pr-2">Date</th>
                    <th className="py-2 pr-2">MR</th>
                    <th className="py-2 pr-2">Product</th>
                    <th className="py-2 pr-2">Qty</th>
                    <th className="py-2 pr-2">Destination</th>
                    <th className="py-2 pr-2">Status</th>
                  </tr>
                </thead>
                <tbody>
                  {orders.map((o) => (
                    <tr key={o.id} className="border-b" style={{ borderColor: C.line }}>
                      <td className="py-2 pr-2 font-mono text-xs">{o.date}</td>
                      <td className="py-2 pr-2">{users.find((u) => u.id === o.mrId)?.name}</td>
                      <td className="py-2 pr-2">{o.product}</td>
                      <td className="py-2 pr-2 font-mono">{o.qty}</td>
                      <td className="py-2 pr-2" style={{ color: C.muted }}>{o.destination}</td>
                      <td className="py-2 pr-2">
                        <Badge tone={o.status === "Delivered" ? "success" : o.status === "Pending" ? "amber" : "teal"}>{o.status}</Badge>
                      </td>
                    </tr>
                  ))}
                </tbody>
              </table>
            </Card>
            {showAddOrder && (
              <Modal title="New order" onClose={() => setShowAddOrder(false)}>
                <AddOrderForm mrList={mrList} products={products} onAdd={(o) => { setOrders((arr) => [o, ...arr]); setShowAddOrder(false); }} onCancel={() => setShowAddOrder(false)} />
              </Modal>
            )}
          </div>
        )}

        {tab === "doctors" && (
          <div>
            <div className="flex items-center justify-between">
              <SectionLabel eyebrow="Field Operations" title="Doctors & Product-wise Sales" />
              <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddDoctor(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="h-fit text-white text-xs font-semibold px-3 py-2 rounded-lg flex items-center gap-1.5 disabled:cursor-not-allowed">
                <Plus size={14} /> Add Doctor / Sale
              </button>
            </div>
            <div className="space-y-3">
              {doctors.map((d) => {
                const total = d.sales.reduce((s, x) => s + x.value, 0);
                return (
                  <Card key={d.id}>
                    <div className="flex items-center justify-between mb-2">
                      <div>
                        <div style={{ color: C.ink }} className="font-semibold">{d.name}</div>
                        <div style={{ color: C.muted }} className="text-xs">{d.hospital} · handled by {users.find((u) => u.id === d.mrId)?.name}</div>
                      </div>
                      <div style={{ color: C.teal }} className="font-mono font-bold">{fmtNPR(total)}</div>
                    </div>
                    <div className="flex flex-wrap gap-2">
                      {d.sales.map((s, i) => (
                        <Badge key={i} tone="amber">{products.find((p) => p.id === s.productId)?.name} · {fmtNPR(s.value)} ({s.month})</Badge>
                      ))}
                    </div>
                  </Card>
                );
              })}
            </div>
            {showAddDoctor && (
              <Modal title="Add doctor / sales entry" onClose={() => setShowAddDoctor(false)}>
                <AddDoctorForm
                  mrList={mrList}
                  products={products}
                  doctors={doctors}
                  onAdd={(d) => { setDoctors(d); setShowAddDoctor(false); }}
                  onCancel={() => setShowAddDoctor(false)}
                />
              </Modal>
            )}
          </div>
        )}

        {tab === "cash" && (
          <div>
            <div className="flex items-center justify-between">
              <SectionLabel eyebrow="Field Operations" title="Cash Collection" />
              <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddCash(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="h-fit text-white text-xs font-semibold px-3 py-2 rounded-lg flex items-center gap-1.5 disabled:cursor-not-allowed">
                <Plus size={14} /> Log Collection
              </button>
            </div>
            <Card>
              <table className="w-full text-left text-sm">
                <thead>
                  <tr style={{ color: C.muted }} className="text-xs font-mono uppercase border-b" style={{ borderColor: C.line }}>
                    <th className="py-2 pr-2">Date</th>
                    <th className="py-2 pr-2">MR</th>
                    <th className="py-2 pr-2">Amount</th>
                    <th className="py-2 pr-2">Note</th>
                  </tr>
                </thead>
                <tbody>
                  {cash.map((c) => (
                    <tr key={c.id} className="border-b" style={{ borderColor: C.line }}>
                      <td className="py-2 pr-2 font-mono text-xs">{c.date}</td>
                      <td className="py-2 pr-2">{users.find((u) => u.id === c.mrId)?.name}</td>
                      <td className="py-2 pr-2 font-mono font-semibold" style={{ color: C.success }}>{fmtNPR(c.amount)}</td>
                      <td className="py-2 pr-2" style={{ color: C.muted }}>{c.note}</td>
                    </tr>
                  ))}
                </tbody>
              </table>
              <div style={{ color: C.ink }} className="mt-3 font-mono text-sm font-semibold">
                Total collected: {fmtNPR(cash.reduce((s, c) => s + c.amount, 0))}
              </div>
            </Card>
            {showAddCash && (
              <Modal title="Log cash collection" onClose={() => setShowAddCash(false)}>
                <AddCashForm mrList={mrList} onAdd={(c) => { setCash((arr) => [c, ...arr]); setShowAddCash(false); }} onCancel={() => setShowAddCash(false)} />
              </Modal>
            )}
          </div>
        )}

        {tab === "comparison" && (
          <div>
            <div className="flex items-center justify-between mb-1">
              <SectionLabel eyebrow="Analytics" title="MR-wise Sales Comparison" />
              <div className="flex gap-1 h-fit">
                {["monthly", "quarterly", "yearly"].map((p) => (
                  <button
                    key={p}
                    onClick={() => setPeriod(p)}
                    style={{ background: period === p ? C.teal : C.surface, color: period === p ? "#fff" : C.text, border: `1px solid ${C.line}` }}
                    className="text-xs font-semibold px-3 py-1.5 rounded-lg capitalize"
                  >
                    {p}
                  </button>
                ))}
              </div>
            </div>
            <Card>
              <ResponsiveContainer width="100%" height={320}>
                <BarChart data={barData}>
                  <CartesianGrid strokeDasharray="3 3" stroke={C.line} />
                  <XAxis dataKey="name" tick={{ fontSize: 11, fill: C.muted }} />
                  <YAxis tick={{ fontSize: 10, fill: C.muted }} tickFormatter={(v) => (v / 1000) + "k"} />
                  <Tooltip formatter={(v) => fmtNPR(v)} />
                  <Legend />
                  <Bar dataKey="Target" fill={C.line} radius={[4, 4, 0, 0]} />
                  <Bar dataKey="Achieved" fill={C.amber} radius={[4, 4, 0, 0]} />
                </BarChart>
              </ResponsiveContainer>
            </Card>
            <Card className="mt-4">
              <table className="w-full text-left text-sm">
                <thead>
                  <tr style={{ color: C.muted }} className="text-xs font-mono uppercase border-b" style={{ borderColor: C.line }}>
                    <th className="py-2 pr-2">MR</th>
                    <th className="py-2 pr-2">Area</th>
                    <th className="py-2 pr-2">Target</th>
                    <th className="py-2 pr-2">Achieved</th>
                    <th className="py-2 pr-2">Variance</th>
                    <th className="py-2 pr-2">%</th>
                  </tr>
                </thead>
                <tbody>
                  {mrList.map((u) => {
                    const variance = u.achieved[period] - u.target[period];
                    return (
                      <tr key={u.id} className="border-b" style={{ borderColor: C.line }}>
                        <td className="py-2 pr-2 font-medium">{u.name}</td>
                        <td className="py-2 pr-2" style={{ color: C.muted }}>{u.area}</td>
                        <td className="py-2 pr-2 font-mono">{fmtNPR(u.target[period])}</td>
                        <td className="py-2 pr-2 font-mono">{fmtNPR(u.achieved[period])}</td>
                        <td className="py-2 pr-2 font-mono flex items-center gap-1" style={{ color: variance >= 0 ? C.success : C.danger }}>
                          {variance >= 0 ? <TrendingUp size={13} /> : <TrendingDown size={13} />} {fmtNPR(Math.abs(variance))}
                        </td>
                        <td className="py-2 pr-2"><Badge tone={pct(u.achieved[period], u.target[period]) >= 100 ? "success" : "amber"}>{pct(u.achieved[period], u.target[period])}%</Badge></td>
                      </tr>
                    );
                  })}
                </tbody>
              </table>
            </Card>
          </div>
        )}

        {tab === "location" && (
          <div>
            <SectionLabel eyebrow="Field Operations" title="Live Location Tracking" />
            <Card>
              <div style={{ color: C.muted }} className="text-xs font-mono mb-4">Demo shows last known check-in per MR. Production build uses live GPS pings from the mobile app, shown on an interactive map.</div>
              <div className="space-y-3">
                {locations.map((l) => {
                  const u = users.find((x) => x.id === l.mrId);
                  return (
                    <div key={l.mrId} style={{ background: C.surfaceAlt }} className="rounded-lg p-3 flex items-center justify-between">
                      <div className="flex items-center gap-3">
                        <div style={{ background: C.tealPale }} className="w-9 h-9 rounded-full flex items-center justify-center">
                          <MapPin size={16} color={C.teal} />
                        </div>
                        <div>
                          <div className="font-medium">{u?.name}</div>
                          <div style={{ color: C.muted }} className="text-xs">{l.area}</div>
                        </div>
                      </div>
                      <div className="text-right">
                        <Badge tone="teal">{l.status}</Badge>
                        <div style={{ color: C.muted }} className="text-[10px] font-mono mt-1">{l.lastSeen}</div>
                      </div>
                    </div>
                  );
                })}
              </div>
            </Card>
          </div>
        )}

        {tab === "visits" && (
          <div>
            <div className="flex items-center justify-between">
              <SectionLabel eyebrow="Field Operations" title="Daily Visit Reports" />
              {session.role === "mr" && (
                <button disabled={session.guest} title={session.guest ? "Guest preview is view-only" : undefined} onClick={() => setShowAddVisit(true)} style={{ background: C.teal, opacity: session.guest ? 0.4 : 1 }} className="h-fit text-white text-xs font-semibold px-3 py-2 rounded-lg flex items-center gap-1.5 disabled:cursor-not-allowed">
                  <Plus size={14} /> Log Today's Visit
                </button>
              )}
            </div>

            {session.role !== "mr" && (
              <Card className="mb-4">
                <div style={{ color: C.ink }} className="font-semibold mb-3">Visits this week — by MR</div>
                <div className="grid grid-cols-3 gap-3">
                  {mrList.map((m) => {
                    const count = visits.filter((v) => v.mrId === m.id).length;
                    return (
                      <div key={m.id} style={{ background: C.surfaceAlt }} className="rounded-lg p-3">
                        <div className="font-medium text-sm">{m.name}</div>
                        <div style={{ color: C.teal }} className="text-2xl font-bold font-mono">{count}</div>
                        <div style={{ color: C.muted }} className="text-[10px] font-mono uppercase">visits logged</div>
                      </div>
                    );
                  })}
                </div>
              </Card>
            )}

            <Card>
              <div className="flex items-center justify-between mb-3">
                <div style={{ color: C.ink }} className="font-semibold">Visit log</div>
                {session.role !== "mr" && (
                  <select value={visitFilterMr} onChange={(e) => setVisitFilterMr(e.target.value)} className="border rounded-lg px-2 py-1 text-xs" style={inputStyle}>
                    <option value="all">All MRs</option>
                    {mrList.map((m) => <option key={m.id} value={m.id}>{m.name}</option>)}
                  </select>
                )}
              </div>
              <table className="w-full text-left text-sm">
                <thead>
                  <tr style={{ color: C.muted }} className="text-xs font-mono uppercase border-b" style={{ borderColor: C.line }}>
                    <th className="py-2 pr-2">Date</th>
                    <th className="py-2 pr-2">MR</th>
                    <th className="py-2 pr-2">Doctor</th>
                    <th className="py-2 pr-2">Hospital</th>
                    <th className="py-2 pr-2">Notes</th>
                  </tr>
                </thead>
                <tbody>
                  {visits
                    .filter((v) => session.role === "mr" ? v.mrId === currentUser?.id : (visitFilterMr === "all" || v.mrId === visitFilterMr))
                    .sort((a, b) => (a.date < b.date ? 1 : -1))
                    .map((v) => (
                      <tr key={v.id} className="border-b" style={{ borderColor: C.line }}>
                        <td className="py-2 pr-2 font-mono text-xs">{v.date}</td>
                        <td className="py-2 pr-2">{users.find((u) => u.id === v.mrId)?.name}</td>
                        <td className="py-2 pr-2">{doctors.find((d) => d.id === v.doctorId)?.name}</td>
                        <td className="py-2 pr-2" style={{ color: C.muted }}>{v.hospital}</td>
                        <td className="py-2 pr-2" style={{ color: C.muted }}>{v.notes}</td>
                      </tr>
                    ))}
                </tbody>
              </table>
            </Card>

            {showAddVisit && (
              <Modal title="Log today's visit" onClose={() => setShowAddVisit(false)}>
                <AddVisitForm
                  mrId={currentUser?.id}
                  doctors={doctors.filter((d) => d.mrId === currentUser?.id)}
                  onAdd={(v) => { setVisits((arr) => [v, ...arr]); setShowAddVisit(false); }}
                  onCancel={() => setShowAddVisit(false)}
                />
              </Modal>
            )}
          </div>
        )}
      </div>
      <Chatbot />
    </div>
  );
}

// ---- Modal wrapper ----
function Modal({ title, children, onClose }) {
  return (
    <div className="fixed inset-0 z-40 flex items-center justify-center p-4" style={{ background: "rgba(15,27,45,0.5)" }}>
      <div style={{ background: C.surface }} className="w-full max-w-md rounded-xl p-6 max-h-[85vh] overflow-y-auto">
        <div className="flex items-center justify-between mb-4">
          <h3 style={{ color: C.ink }} className="font-bold">{title}</h3>
          <button onClick={onClose}><X size={18} color={C.muted} /></button>
        </div>
        {children}
      </div>
    </div>
  );
}

function Field({ label, children }) {
  return (
    <div className="mb-3">
      <div style={{ color: C.muted }} className="text-xs font-mono uppercase tracking-wide mb-1">{label}</div>
      {children}
    </div>
  );
}
const inputStyle = { borderColor: C.line };

function AddUserForm({ users, onAdd, onCancel }) {
  const [name, setName] = useState("");
  const [role, setRole] = useState("mr");
  const [region, setRegion] = useState("");
  const [area, setArea] = useState("");
  const [manager, setManager] = useState("");
  const [email, setEmail] = useState("");

  return (
    <div>
      <Field label="Full name"><input value={name} onChange={(e) => setName(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Role">
        <select value={role} onChange={(e) => setRole(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {ROLES.map((r) => <option key={r.key} value={r.key}>{r.label}</option>)}
        </select>
      </Field>
      <Field label="Region"><input value={region} onChange={(e) => setRegion(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Area"><input value={area} onChange={(e) => setArea(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Reports to">
        <select value={manager} onChange={(e) => setManager(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          <option value="">—</option>
          {users.map((u) => <option key={u.id} value={u.name}>{u.name}</option>)}
        </select>
      </Field>
      <Field label="Gmail"><input value={email} onChange={(e) => setEmail(e.target.value)} placeholder="name@gmail.com" className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button
          disabled={!name}
          onClick={() => onAdd({ id: "u" + Date.now(), name, role, region, area, manager, email, target: { monthly: 0, quarterly: 0, yearly: 0 }, achieved: { monthly: 0, quarterly: 0, yearly: 0 } })}
          style={{ background: C.teal }}
          className="flex-1 text-white rounded-lg py-2 text-sm font-semibold disabled:opacity-40"
        >
          Add profile
        </button>
      </div>
    </div>
  );
}

function AddProductForm({ onAdd, onCancel }) {
  const [name, setName] = useState("");
  const [division, setDivision] = useState("");
  return (
    <div>
      <Field label="Product name"><input value={name} onChange={(e) => setName(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Division"><input value={division} onChange={(e) => setDivision(e.target.value)} placeholder="e.g. Oncology, Nutraceutical" className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button disabled={!name || !division} onClick={() => onAdd({ id: "p" + Date.now(), name, division })} style={{ background: C.teal }} className="flex-1 text-white rounded-lg py-2 text-sm font-semibold disabled:opacity-40">Add product</button>
      </div>
    </div>
  );
}

function AddOrderForm({ mrList, products, onAdd, onCancel }) {
  const [mrId, setMrId] = useState(mrList[0]?.id || "");
  const [product, setProduct] = useState(products[0]?.name || "");
  const [qty, setQty] = useState(10);
  const [destination, setDestination] = useState("Company - Direct");
  return (
    <div>
      <Field label="Marketing representative">
        <select value={mrId} onChange={(e) => setMrId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {mrList.map((m) => <option key={m.id} value={m.id}>{m.name}</option>)}
        </select>
      </Field>
      <Field label="Product">
        <select value={product} onChange={(e) => setProduct(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {products.map((p) => <option key={p.id} value={p.name}>{p.name}</option>)}
        </select>
      </Field>
      <Field label="Quantity"><input type="number" value={qty} onChange={(e) => setQty(Number(e.target.value))} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Order from">
        <select value={destination} onChange={(e) => setDestination(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          <option>Company - Direct</option>
          <option>Stockist - Everest Pharma Distributors</option>
          <option>Stockist - Local Market Stockist</option>
        </select>
      </Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button
          onClick={() => onAdd({ id: "o" + Date.now(), mrId, product, qty, destination, status: "Pending", date: new Date().toISOString().slice(0, 10) })}
          style={{ background: C.teal }}
          className="flex-1 text-white rounded-lg py-2 text-sm font-semibold"
        >
          Place order
        </button>
      </div>
    </div>
  );
}

function AddDoctorForm({ mrList, products, doctors, onAdd, onCancel }) {
  const [mode, setMode] = useState("new"); // new doctor or existing
  const [existingId, setExistingId] = useState(doctors[0]?.id || "");
  const [name, setName] = useState("");
  const [hospital, setHospital] = useState("");
  const [mrId, setMrId] = useState(mrList[0]?.id || "");
  const [productId, setProductId] = useState(products[0]?.id || "");
  const [value, setValue] = useState(10000);

  const submit = () => {
    const month = new Date().toISOString().slice(0, 7);
    if (mode === "new") {
      onAdd([...doctors, { id: "d" + Date.now(), name, hospital, mrId, sales: [{ productId, value, month }] }]);
    } else {
      onAdd(doctors.map((d) => d.id === existingId ? { ...d, sales: [...d.sales, { productId, value, month }] } : d));
    }
  };

  return (
    <div>
      <div className="flex gap-2 mb-3">
        <button onClick={() => setMode("new")} style={{ background: mode === "new" ? C.teal : C.surface, color: mode === "new" ? "#fff" : C.text, border: `1px solid ${C.line}` }} className="flex-1 rounded-lg py-2 text-xs font-semibold">New doctor</button>
        <button onClick={() => setMode("existing")} style={{ background: mode === "existing" ? C.teal : C.surface, color: mode === "existing" ? "#fff" : C.text, border: `1px solid ${C.line}` }} className="flex-1 rounded-lg py-2 text-xs font-semibold">Log sale for existing</button>
      </div>
      {mode === "new" ? (
        <>
          <Field label="Doctor name"><input value={name} onChange={(e) => setName(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
          <Field label="Hospital / clinic"><input value={hospital} onChange={(e) => setHospital(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
          <Field label="Handled by">
            <select value={mrId} onChange={(e) => setMrId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
              {mrList.map((m) => <option key={m.id} value={m.id}>{m.name}</option>)}
            </select>
          </Field>
        </>
      ) : (
        <Field label="Doctor">
          <select value={existingId} onChange={(e) => setExistingId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
            {doctors.map((d) => <option key={d.id} value={d.id}>{d.name}</option>)}
          </select>
        </Field>
      )}
      <Field label="Product">
        <select value={productId} onChange={(e) => setProductId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {products.map((p) => <option key={p.id} value={p.id}>{p.name}</option>)}
        </select>
      </Field>
      <Field label="Sales value (NPR)"><input type="number" value={value} onChange={(e) => setValue(Number(e.target.value))} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button disabled={mode === "new" && (!name || !hospital)} onClick={submit} style={{ background: C.teal }} className="flex-1 text-white rounded-lg py-2 text-sm font-semibold disabled:opacity-40">Save</button>
      </div>
    </div>
  );
}

function AddHospitalForm({ onAdd, onCancel }) {
  const [name, setName] = useState("");
  return (
    <div>
      <Field label="Hospital name"><input value={name} onChange={(e) => setName(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button disabled={!name} onClick={() => onAdd({ id: "h" + Date.now(), name })} style={{ background: C.teal }} className="flex-1 text-white rounded-lg py-2 text-sm font-semibold disabled:opacity-40">Add hospital</button>
      </div>
    </div>
  );
}

function AddPrescriberForm({ mrList, hospitals, onAdd, onCancel }) {
  const [name, setName] = useState("");
  const [hospital, setHospital] = useState(hospitals[0]?.name || "");
  const [mrId, setMrId] = useState(mrList[0]?.id || "");
  return (
    <div>
      <Field label="Doctor name"><input value={name} onChange={(e) => setName(e.target.value)} placeholder="Dr. ..." className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Hospital">
        <select value={hospital} onChange={(e) => setHospital(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {hospitals.map((h) => <option key={h.id} value={h.name}>{h.name}</option>)}
        </select>
      </Field>
      <Field label="Handled by">
        <select value={mrId} onChange={(e) => setMrId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {mrList.map((m) => <option key={m.id} value={m.id}>{m.name}</option>)}
        </select>
      </Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button disabled={!name} onClick={() => onAdd({ id: "d" + Date.now(), name, hospital, mrId, sales: [] })} style={{ background: C.teal }} className="flex-1 text-white rounded-lg py-2 text-sm font-semibold disabled:opacity-40">Add prescriber</button>
      </div>
    </div>
  );
}

function AddVisitForm({ mrId, doctors, onAdd, onCancel }) {
  const [date, setDate] = useState(new Date().toISOString().slice(0, 10));
  const [doctorId, setDoctorId] = useState(doctors[0]?.id || "");
  const [notes, setNotes] = useState("");
  const selectedDoctor = doctors.find((d) => d.id === doctorId);
  return (
    <div>
      <Field label="Date"><input type="date" value={date} onChange={(e) => setDate(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Doctor visited">
        <select value={doctorId} onChange={(e) => setDoctorId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {doctors.length === 0 && <option value="">No doctors assigned yet</option>}
          {doctors.map((d) => <option key={d.id} value={d.id}>{d.name} — {d.hospital}</option>)}
        </select>
      </Field>
      <Field label="Notes"><textarea value={notes} onChange={(e) => setNotes(e.target.value)} rows={3} placeholder="What was discussed, samples left, follow-up needed..." className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button
          disabled={!doctorId}
          onClick={() => onAdd({ id: "v" + Date.now(), mrId, date, doctorId, hospital: selectedDoctor?.hospital || "", notes })}
          style={{ background: C.teal }}
          className="flex-1 text-white rounded-lg py-2 text-sm font-semibold disabled:opacity-40"
        >
          Submit visit
        </button>
      </div>
    </div>
  );
}

function AddCashForm({ mrList, onAdd, onCancel }) {
  const [mrId, setMrId] = useState(mrList[0]?.id || "");
  const [amount, setAmount] = useState(10000);
  const [note, setNote] = useState("");
  return (
    <div>
      <Field label="Marketing representative">
        <select value={mrId} onChange={(e) => setMrId(e.target.value)} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle}>
          {mrList.map((m) => <option key={m.id} value={m.id}>{m.name}</option>)}
        </select>
      </Field>
      <Field label="Amount collected (NPR)"><input type="number" value={amount} onChange={(e) => setAmount(Number(e.target.value))} className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <Field label="Note"><input value={note} onChange={(e) => setNote(e.target.value)} placeholder="e.g. area / pharmacy visited" className="w-full border rounded-lg px-3 py-2 text-sm" style={inputStyle} /></Field>
      <div className="flex gap-2 mt-4">
        <button onClick={onCancel} className="flex-1 border rounded-lg py-2 text-sm" style={inputStyle}>Cancel</button>
        <button
          onClick={() => onAdd({ id: "c" + Date.now(), mrId, amount, note, date: new Date().toISOString().slice(0, 10) })}
          style={{ background: C.teal }}
          className="flex-1 text-white rounded-lg py-2 text-sm font-semibold"
        >
          Log collection
        </button>
      </div>
    </div>
  );
}
