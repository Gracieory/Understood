import { useState, useRef, useCallback } from "react";

const C = {
  cream: "#F5F0E8", linen: "#EDE4D3", stone: "#D4C5A9",
  warmText: "#3D2E1A", mutedText: "#7A6A52",
  accent: "#C17A3A", accentLight: "#F0DFC0",
  redWarm: "#C0392B", redLight: "#FDECEA",
  greenWarm: "#2E7D52", greenLight: "#E8F5EE",
  blueWarm: "#1A5C8A", blueLight: "#E6F0F8",
  purpleWarm: "#5C3A8A", purpleLight: "#F0EBF8",
};

const FONT = "'PingFang SC','Hiragino Sans GB','Microsoft YaHei',sans-serif";

const BASE = {
  app: {
    minHeight: "100vh",
    background: `linear-gradient(155deg, ${C.cream} 0%, ${C.linen} 100%)`,
    fontFamily: FONT, color: C.warmText, position: "relative",
  },
  grain: {
    position: "fixed", inset: 0,
    backgroundImage: `url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.025'/%3E%3C/svg%3E")`,
    pointerEvents: "none", zIndex: 1,
  },
  page: { maxWidth: 520, margin: "0 auto", padding: "36px 20px 80px", position: "relative", zIndex: 2 },
};

// ─── SHARED COMPONENTS ────────────────────────────────────────────────────────

function BackBtn({ onBack }) {
  return (
    <button onClick={onBack} style={{
      background: "rgba(255,255,255,0.6)", border: `1px solid ${C.stone}50`,
      borderRadius: 50, padding: "8px 20px", fontSize: 16, color: C.mutedText,
      cursor: "pointer", fontFamily: FONT, marginBottom: 28, display: "flex",
      alignItems: "center", gap: 6,
    }}>← 返回首页</button>
  );
}

function InfoCard({ icon, label, text, color = C.accentLight, textColor = C.warmText, labelColor = C.mutedText }) {
  return (
    <div style={{
      background: color, borderRadius: 18, padding: "16px 18px",
      marginBottom: 12, display: "flex", gap: 14, alignItems: "flex-start",
    }}>
      <div style={{
        width: 42, height: 42, borderRadius: "50%", background: "rgba(255,255,255,0.65)",
        display: "flex", alignItems: "center", justifyContent: "center",
        fontSize: 20, flexShrink: 0,
      }}>{icon}</div>
      <div>
        <div style={{ fontSize: 13, color: labelColor, fontWeight: 600, marginBottom: 4 }}>{label}</div>
        <div style={{ fontSize: 19, fontWeight: 700, color: textColor, lineHeight: 1.55 }}>{text}</div>
      </div>
    </div>
  );
}

function Dots() {
  return (
    <div style={{ display: "flex", gap: 10, justifyContent: "center", margin: "24px 0" }}>
      {[0, 0.2, 0.4].map((d, i) => (
        <div key={i} style={{
          width: 13, height: 13, borderRadius: "50%", background: C.accent,
          animation: "pulse 1.4s ease-in-out infinite", animationDelay: `${d}s`, opacity: 0.7,
        }} />
      ))}
    </div>
  );
}

function ResetBtn({ onClick, label = "↩ 重新来一次" }) {
  return (
    <button onClick={onClick} style={{
      width: "100%", marginTop: 12, background: "transparent",
      color: C.mutedText, border: `1.5px solid ${C.stone}`,
      borderRadius: 50, padding: "14px 0", fontSize: 18,
      cursor: "pointer", fontFamily: FONT,
    }}>{label}</button>
  );
}

// ─── HOME ────────────────────────────────────────────────────────────────────

const MODULES = [
  {
    id: "meds",
    emoji: "💊",
    title: "看药品说明",
    desc: "拍一张药盒，AI 告诉您怎么吃",
    bg: C.accentLight,
    border: `${C.accent}40`,
    badge: "最常用",
    badgeBg: C.accent,
  },
  {
    id: "fraud",
    emoji: "🛡️",
    title: "防骗安全查验",
    desc: "收到可疑消息？让 AI 帮您判断",
    bg: C.redLight,
    border: `${C.redWarm}30`,
    badge: "保护您",
    badgeBg: C.redWarm,
  },
  {
    id: "guide",
    emoji: "📱",
    title: "手机操作指南",
    desc: "不会用手机某功能？问 AI 就够了",
    bg: C.blueLight,
    border: `${C.blueWarm}30`,
    badge: "随时问",
    badgeBg: C.blueWarm,
  },
];

function Home({ onNav }) {
  const now = new Date();
  const hour = now.getHours();
  const greeting = hour < 12 ? "早上好" : hour < 18 ? "下午好" : "晚上好";

  return (
    <div style={BASE.page}>
      <div style={{ textAlign: "center", marginBottom: 40 }}>
        <div style={{ fontSize: 52, marginBottom: 10 }}>🌿</div>
        <div style={{ fontSize: 30, fontWeight: 800, color: C.warmText, letterSpacing: "0.04em" }}>
          长辈助手
        </div>
        <div style={{ fontSize: 17, color: C.mutedText, marginTop: 6, lineHeight: 1.6 }}>
          {greeting}，有什么需要帮忙的？
        </div>
      </div>

      {MODULES.map((m, i) => (
        <div
          key={m.id}
          onClick={() => onNav(m.id)}
          style={{
            background: `rgba(255,255,255,0.62)`,
            border: `1.5px solid ${m.border}`,
            borderRadius: 24, padding: "22px 22px",
            marginBottom: 14, cursor: "pointer",
            display: "flex", alignItems: "center", gap: 18,
            backdropFilter: "blur(8px)",
            animation: `fadeUp 0.4s ${i * 0.08}s ease both`,
            opacity: 0,
            transition: "transform 0.18s, box-shadow 0.18s",
          }}
          onMouseEnter={e => e.currentTarget.style.transform = "translateY(-2px)"}
          onMouseLeave={e => e.currentTarget.style.transform = "translateY(0)"}
        >
          <div style={{
            width: 64, height: 64, borderRadius: 20,
            background: m.bg, display: "flex",
            alignItems: "center", justifyContent: "center",
            fontSize: 30, flexShrink: 0,
          }}>{m.emoji}</div>
          <div style={{ flex: 1 }}>
            <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 5 }}>
              <span style={{ fontSize: 22, fontWeight: 800, color: C.warmText }}>{m.title}</span>
              <span style={{
                background: m.badgeBg, color: "#fff",
                fontSize: 12, fontWeight: 700, padding: "2px 10px",
                borderRadius: 50, letterSpacing: "0.04em",
              }}>{m.badge}</span>
            </div>
            <div style={{ fontSize: 16, color: C.mutedText, lineHeight: 1.5 }}>{m.desc}</div>
          </div>
          <div style={{ fontSize: 22, color: C.stone, flexShrink: 0 }}>›</div>
        </div>
      ))}

      <div style={{
        marginTop: 32, background: "rgba(255,255,255,0.45)",
        borderRadius: 20, padding: "18px 20px",
        border: `1px solid ${C.stone}30`,
        textAlign: "center",
      }}>
        <div style={{ fontSize: 14, color: C.mutedText, lineHeight: 1.8 }}>
          💬 &nbsp;这个 App 是家人为您准备的<br />
          有任何问题，直接开口说或者点一点就好
        </div>
      </div>
    </div>
  );
}

// ─── MODULE 1: MEDICATION ─────────────────────────────────────────────────────

const AUTH_CONFIG = {
  genuine:    { bg: "#E8F5EE", border: "#2E7D5240", icon: "✅", label: "正规药品",    color: "#2E7D52" },
  suspicious: { bg: "#FFF3E0", border: "#E65100",   icon: "⚠️", label: "存在疑点",    color: "#BF360C" },
  unknown:    { bg: "#F3F3F3", border: "#78787840",  icon: "❓", label: "无法完全判断", color: "#555" },
};

async function analyzeMeds(base64, mime) {
  const sys = `你是一位专业的全球药品识别专家兼温柔护工阿姨。你能识别任何语言的药盒（中文、英文、日文、韩文、法文、德文、阿拉伯文、西班牙文等），并翻译成中文大白话解释给老年人听。

两个核心任务：
1. 多语言识别：无论药盒是什么语言，准确提取药品信息并用中文大白话解释
2. 真伪鉴别：根据批准文号格式、厂家、包装规范性等多维度判断真伪风险

返回JSON（不含代码块标记）：
{
  "detectedLang": "识别到的语言，如中文、英文、日文、多语言混合",
  "drugName": "中文通用名（最简单叫法）",
  "originalName": "药盒原始名称（保留原文字母/汉字）",
  "englishName": "英文通用名或品牌名（如有则填，否则填null）",
  "manufacturer": "生产厂家名称",
  "manufacturerCountry": "生产国",
  "approvalNo": "批准文号或注册号原文（如国药准字H20010024 / NDC 0071-0155-23）",
  "batchNo": "批号原文（如可见，否则null）",
  "expiryDate": "有效期原文（如可见，否则null）",
  "effect": "一句话说清楚治什么病",
  "dosage": "怎么吃：几片，一天几次，饭前饭后",
  "storage": "怎么保存",
  "warnings": ["注意事项1", "注意事项2"],
  "authenticityLevel": "genuine | suspicious | unknown",
  "authenticityDetails": ["真伪判断依据1", "依据2", "依据3"],
  "authenticityAdvice": "关于真伪的家人口吻建议",
  "safeInfo": "一句放心提示（genuine时写，suspicious时不写）",
  "speakText": "用温暖口吻对老人说的总结"
}

真伪判断依据（多维度综合）：
- 批准文号格式规范性（中国：国药准字[H/Z/S/J]8位数字；美国NDC：5-4-2或5-3-2格式；欧盟：EU/1/开头）
- 厂家是否为已知正规药企
- 包装文字印刷清晰度和专业性
- 有效期格式是否标准
- 成分/说明书是否完整
- 是否有明显低质量包装迹象`;

  const res = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST", headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-20250514", max_tokens: 1500, system: sys,
      messages: [{ role: "user", content: [
        { type: "image", source: { type: "base64", media_type: mime, data: base64 } },
        { type: "text", text: "请帮我识别分析这个药品，包括语言识别和真伪鉴别。" }
      ]}]
    })
  });
  if (!res.ok) throw new Error(`请求失败 ${res.status}`);
  const d = await res.json();
  return JSON.parse(d.content.map(b => b.text || "").join("").replace(/```json|```/g, "").trim());
}

function MedsModule({ onBack }) {
  const [phase, setPhase] = useState("upload");
  const [img, setImg] = useState(null);
  const [b64, setB64] = useState(null);
  const [mime, setMime] = useState(null);
  const [result, setResult] = useState(null);
  const [err, setErr] = useState(null);
  const fileRef = useRef();

  const loadFile = useCallback(file => {
    if (!file?.type.startsWith("image/")) return;
    const r = new FileReader();
    r.onload = e => {
      setImg(e.target.result);
      setB64(e.target.result.split(",")[1]);
      setMime(file.type);
      setPhase("preview");
    };
    r.readAsDataURL(file);
  }, []);

  const analyze = async () => {
    setPhase("loading");
    try { setResult(await analyzeMeds(b64, mime)); setPhase("result"); }
    catch (e) { setErr(e.message); setPhase("error"); }
  };

  const reset = () => { setPhase("upload"); setImg(null); setB64(null); setResult(null); setErr(null); };

  return (
    <div style={BASE.page}>
      <BackBtn onBack={onBack} />
      <div style={{ textAlign: "center", marginBottom: 32 }}>
        <div style={{ fontSize: 48 }}>💊</div>
        <div style={{ fontSize: 28, fontWeight: 800, marginTop: 8 }}>药品说明助手</div>
        <div style={{ fontSize: 16, color: C.mutedText, marginTop: 6 }}>拍一张药盒，马上看懂怎么吃</div>
      </div>

      {phase === "upload" && (
        <div onClick={() => fileRef.current?.click()} style={{
          background: "rgba(255,255,255,0.65)", border: `2px dashed ${C.stone}`,
          borderRadius: 24, padding: "44px 20px", textAlign: "center", cursor: "pointer",
          backdropFilter: "blur(8px)",
        }}>
          <div style={{ fontSize: 60, marginBottom: 16 }}>📷</div>
          <div style={{ fontSize: 22, fontWeight: 700, marginBottom: 8 }}>点这里拍照</div>
          <div style={{ fontSize: 16, color: C.mutedText, lineHeight: 1.7 }}>
            看不懂没关系<br />AI 来帮您，一句话说清楚怎么吃
          </div>
          <div style={{
            marginTop: 24, background: C.accent, color: "#FFF8F0",
            borderRadius: 50, padding: "16px 40px", fontSize: 20, fontWeight: 700,
            display: "inline-block",
          }}>选择照片 / 拍照</div>
          <input ref={fileRef} type="file" accept="image/*" capture="environment"
            style={{ display: "none" }} onChange={e => loadFile(e.target.files[0])} />
        </div>
      )}

      {phase === "preview" && (
        <div style={{ background: "rgba(255,255,255,0.65)", borderRadius: 24, padding: 18, backdropFilter: "blur(8px)" }}>
          <img src={img} alt="药盒" style={{ width: "100%", borderRadius: 16, maxHeight: 260, objectFit: "cover", display: "block" }} />
          <button onClick={analyze} style={{
            width: "100%", marginTop: 14, background: C.accent, color: "#FFF8F0",
            border: "none", borderRadius: 50, padding: "18px 0", fontSize: 22,
            fontWeight: 700, cursor: "pointer", fontFamily: FONT,
          }}>🔍 &nbsp;分析这个药</button>
          <ResetBtn onClick={reset} label="重新拍一张" />
        </div>
      )}

      {phase === "loading" && (
        <div style={{ textAlign: "center", padding: "60px 0" }}>
          <div style={{ fontSize: 56 }}>🤔</div>
          <Dots />
          <div style={{ fontSize: 20, color: C.mutedText }}>正在仔细看这个药盒…<br /><span style={{ fontSize: 16 }}>马上就好，请稍等一下</span></div>
        </div>
      )}

      {phase === "result" && result && (() => {
        const ac = AUTH_CONFIG[result.authenticityLevel] || AUTH_CONFIG.unknown;
        return (
        <div>
          {/* 药品名称块 */}
          <div style={{ background: "rgba(255,255,255,0.72)", borderRadius: 26, padding: "24px 22px", backdropFilter: "blur(12px)", border: `1px solid ${C.stone}30`, marginBottom: 12 }}>
            <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 14 }}>
              <span style={{ background: C.accentLight, borderRadius: 50, padding: "3px 12px", fontSize: 13, color: C.accent, fontWeight: 700 }}>
                {result.detectedLang || "药品"}
              </span>
            </div>
            <div style={{ fontSize: 32, fontWeight: 900, lineHeight: 1.15, color: C.warmText }}>{result.drugName}</div>
            {result.originalName && result.originalName !== result.drugName && (
              <div style={{ fontSize: 16, color: C.mutedText, marginTop: 4, fontStyle: "italic" }}>{result.originalName}</div>
            )}
            {result.englishName && (
              <div style={{ fontSize: 15, color: C.mutedText, marginTop: 2 }}>{result.englishName}</div>
            )}
            {result.effect && <div style={{ fontSize: 17, color: C.warmText, marginTop: 10, lineHeight: 1.5, padding: "10px 0 0", borderTop: `1px solid ${C.linen}` }}>{result.effect}</div>}
          </div>

          {/* 真伪鉴定块 */}
          <div style={{ background: ac.bg, border: `2px solid ${ac.border}`, borderRadius: 22, padding: "20px 22px", marginBottom: 12 }}>
            <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 12 }}>
              <span style={{ fontSize: 26 }}>{ac.icon}</span>
              <div>
                <div style={{ fontSize: 13, color: ac.color, fontWeight: 700 }}>真伪鉴定结果</div>
                <div style={{ fontSize: 22, fontWeight: 900, color: ac.color }}>{ac.label}</div>
              </div>
            </div>
            {result.authenticityDetails?.map((d, i) => (
              <div key={i} style={{ display: "flex", gap: 8, alignItems: "flex-start", marginBottom: 6 }}>
                <span style={{ color: ac.color, fontSize: 14, marginTop: 3, flexShrink: 0 }}>•</span>
                <span style={{ fontSize: 16, color: C.warmText, lineHeight: 1.5 }}>{d}</span>
              </div>
            ))}
            {result.authenticityAdvice && (
              <div style={{ marginTop: 12, paddingTop: 12, borderTop: `1px solid ${ac.color}20`, fontSize: 16, color: ac.color, lineHeight: 1.6, fontWeight: 500 }}>
                {result.authenticityAdvice}
              </div>
            )}
          </div>

          {/* 药品信息块 */}
          <div style={{ background: "rgba(255,255,255,0.68)", borderRadius: 22, padding: "18px 20px", backdropFilter: "blur(8px)", marginBottom: 12, border: `1px solid ${C.stone}20` }}>
            <div style={{ fontSize: 13, color: C.mutedText, fontWeight: 700, marginBottom: 12, letterSpacing: "0.06em" }}>📋 药品档案</div>
            {[
              { label: "生产厂家", val: result.manufacturer },
              { label: "生产国", val: result.manufacturerCountry },
              { label: "批准文号", val: result.approvalNo },
              { label: "批号", val: result.batchNo },
              { label: "有效期", val: result.expiryDate },
            ].filter(r => r.val && r.val !== "null").map((row, i) => (
              <div key={i} style={{ display: "flex", justifyContent: "space-between", padding: "8px 0", borderBottom: `1px solid ${C.linen}`, gap: 12 }}>
                <span style={{ fontSize: 15, color: C.mutedText, flexShrink: 0 }}>{row.label}</span>
                <span style={{ fontSize: 15, color: C.warmText, fontWeight: 600, textAlign: "right", wordBreak: "break-all" }}>{row.val}</span>
              </div>
            ))}
          </div>

          {result.dosage && <InfoCard icon="🕐" label="怎么吃 / 用法用量" text={result.dosage} />}
          {result.storage && <InfoCard icon="📦" label="怎么保存" text={result.storage} />}
          {result.warnings?.map((w, i) => <InfoCard key={i} icon="⚠️" label="注意事项" text={w} color={C.redLight} textColor={C.redWarm} labelColor={C.redWarm} />)}
          {result.safeInfo && <InfoCard icon="✅" label="放心提示" text={result.safeInfo} color={C.greenLight} textColor={C.greenWarm} labelColor={C.greenWarm} />}
          {result.speakText && (
            <div style={{ background: `linear-gradient(135deg, ${C.linen}, ${C.cream})`, borderRadius: 20, padding: "18px 20px", border: `1.5px solid ${C.stone}40`, marginBottom: 12 }}>
              <div style={{ fontSize: 13, color: C.mutedText, fontWeight: 600, marginBottom: 6 }}>👵  AI 用大白话说</div>
              <div style={{ fontSize: 18, lineHeight: 1.8, fontWeight: 500 }}>"{result.speakText}"</div>
            </div>
          )}
          <ResetBtn onClick={reset} label="↩ 重新拍一张药盒" />
        </div>
        );
      })()}

      {phase === "error" && (
        <div>
          <div style={{ background: C.redLight, borderRadius: 18, padding: "20px 22px", border: `1.5px solid ${C.redWarm}20` }}>
            <div style={{ fontSize: 28, marginBottom: 8 }}>😔</div>
            <div style={{ fontSize: 17, color: C.redWarm, lineHeight: 1.6 }}>分析时遇到问题：<br /><strong>{err}</strong><br /><br />请检查照片是否清晰，稍后再试。</div>
          </div>
          <ResetBtn onClick={reset} label="↩ 重新拍一张" />
        </div>
      )}
    </div>
  );
}

// ─── MODULE 2: ANTI-FRAUD ─────────────────────────────────────────────────────

const FRAUD_EXAMPLES = [
  "您好，您的包裹因违禁品被扣押，请立即联系公安局配合调查，否则将依法逮捕...",
  "恭喜您中奖了！您获得了价值5万元的大奖，请点击链接领取，需缴纳200元手续费...",
  "我是您儿子的朋友，他出了点事在医院，现在需要您立刻转账1万元应急...",
];

async function analyzeFraud(text) {
  const sys = `你是专门帮助老年人防范电信诈骗的安全顾问，像一个关心长辈的家人一样说话。
分析用户提供的消息内容，返回JSON（不含代码块标记）：
{"level":"red|yellow|green","levelText":"高风险|需注意|基本安全","summary":"一句话总结风险","tactics":["识别到的诈骗手法1","手法2"],"advice":"用家人口吻给出建议，温暖不生硬","action":"最建议做的一步操作"}
red=明确诈骗, yellow=可疑需谨慎, green=正常信息`;
  const res = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST", headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-20250514", max_tokens: 800, system: sys,
      messages: [{ role: "user", content: `请帮我分析这条消息是否是诈骗：\n\n${text}` }]
    })
  });
  if (!res.ok) throw new Error(`请求失败 ${res.status}`);
  const d = await res.json();
  return JSON.parse(d.content.map(b => b.text || "").join("").replace(/```json|```/g, "").trim());
}

const LEVEL_CONFIG = {
  red: { bg: C.redLight, border: `${C.redWarm}40`, textColor: C.redWarm, icon: "🚨", label: "高风险" },
  yellow: { bg: "#FFFBE6", border: "#F0C040", textColor: "#7A5C00", icon: "⚠️", label: "需注意" },
  green: { bg: C.greenLight, border: `${C.greenWarm}40`, textColor: C.greenWarm, icon: "✅", label: "基本安全" },
};

function FraudModule({ onBack }) {
  const [text, setText] = useState("");
  const [phase, setPhase] = useState("input");
  const [result, setResult] = useState(null);
  const [err, setErr] = useState(null);

  const analyze = async () => {
    if (!text.trim()) return;
    setPhase("loading");
    try { setResult(await analyzeFraud(text)); setPhase("result"); }
    catch (e) { setErr(e.message); setPhase("error"); }
  };

  const reset = () => { setPhase("input"); setText(""); setResult(null); setErr(null); };

  const lc = result ? (LEVEL_CONFIG[result.level] || LEVEL_CONFIG.yellow) : null;

  return (
    <div style={BASE.page}>
      <BackBtn onBack={onBack} />
      <div style={{ textAlign: "center", marginBottom: 32 }}>
        <div style={{ fontSize: 48 }}>🛡️</div>
        <div style={{ fontSize: 28, fontWeight: 800, marginTop: 8 }}>防骗安全查验</div>
        <div style={{ fontSize: 16, color: C.mutedText, marginTop: 6, lineHeight: 1.6 }}>
          收到可疑短信或电话？<br />把内容粘贴进来，AI 帮您判断
        </div>
      </div>

      {phase === "input" && (
        <div>
          <div style={{ background: "rgba(255,255,255,0.65)", borderRadius: 24, padding: 20, backdropFilter: "blur(8px)" }}>
            <div style={{ fontSize: 16, color: C.mutedText, marginBottom: 10, fontWeight: 600 }}>把可疑的消息粘贴在这里 👇</div>
            <textarea
              value={text} onChange={e => setText(e.target.value)}
              placeholder="例如：&quot;您的快递被扣押，请立刻联系公安局配合调查…&quot;"
              style={{
                width: "100%", minHeight: 140, fontSize: 17, lineHeight: 1.7,
                border: `1.5px solid ${C.stone}60`, borderRadius: 16, padding: "14px 16px",
                fontFamily: FONT, color: C.warmText, background: "rgba(255,255,255,0.8)",
                resize: "vertical", boxSizing: "border-box",
              }}
            />
            <button onClick={analyze} disabled={!text.trim()} style={{
              width: "100%", marginTop: 12, background: text.trim() ? C.redWarm : C.stone,
              color: "#fff", border: "none", borderRadius: 50, padding: "18px 0",
              fontSize: 21, fontWeight: 700, cursor: text.trim() ? "pointer" : "default",
              fontFamily: FONT, transition: "background 0.2s",
            }}>🔍 &nbsp;立刻查验这条消息</button>
          </div>

          <div style={{ marginTop: 20 }}>
            <div style={{ fontSize: 14, color: C.mutedText, marginBottom: 10, paddingLeft: 4, fontWeight: 600 }}>常见诈骗消息示例（点击试试）</div>
            {FRAUD_EXAMPLES.map((ex, i) => (
              <div key={i} onClick={() => setText(ex)} style={{
                background: "rgba(255,255,255,0.5)", border: `1px solid ${C.stone}40`,
                borderRadius: 14, padding: "12px 16px", marginBottom: 8, cursor: "pointer",
                fontSize: 14, color: C.mutedText, lineHeight: 1.6,
                overflow: "hidden", textOverflow: "ellipsis", whiteSpace: "nowrap",
              }}>{ex}</div>
            ))}
          </div>
        </div>
      )}

      {phase === "loading" && (
        <div style={{ textAlign: "center", padding: "60px 0" }}>
          <div style={{ fontSize: 56 }}>🔍</div>
          <Dots />
          <div style={{ fontSize: 20, color: C.mutedText }}>正在分析这条消息…<br /><span style={{ fontSize: 16 }}>请稍等，马上出结果</span></div>
        </div>
      )}

      {phase === "result" && result && lc && (
        <div>
          <div style={{
            background: lc.bg, border: `2px solid ${lc.border}`,
            borderRadius: 28, padding: "26px 22px", marginBottom: 14,
            textAlign: "center",
          }}>
            <div style={{ fontSize: 56, marginBottom: 8 }}>{lc.icon}</div>
            <div style={{ fontSize: 30, fontWeight: 900, color: lc.textColor, letterSpacing: "0.04em" }}>
              {lc.label}
            </div>
            <div style={{ fontSize: 18, color: lc.textColor, marginTop: 8, lineHeight: 1.6, fontWeight: 500 }}>
              {result.summary}
            </div>
          </div>

          {result.tactics?.length > 0 && (
            <div style={{ background: "rgba(255,255,255,0.65)", borderRadius: 20, padding: "18px 20px", marginBottom: 14, backdropFilter: "blur(8px)" }}>
              <div style={{ fontSize: 14, color: C.mutedText, fontWeight: 700, marginBottom: 10 }}>识别到的诈骗手法</div>
              {result.tactics.map((t, i) => (
                <div key={i} style={{ display: "flex", gap: 8, alignItems: "flex-start", marginBottom: 6 }}>
                  <span style={{ color: C.redWarm, fontSize: 16, marginTop: 2 }}>•</span>
                  <span style={{ fontSize: 17, color: C.warmText, lineHeight: 1.5 }}>{t}</span>
                </div>
              ))}
            </div>
          )}

          {result.advice && (
            <div style={{ background: `linear-gradient(135deg, ${C.linen}, ${C.cream})`, borderRadius: 20, padding: "18px 20px", marginBottom: 14, border: `1.5px solid ${C.stone}40` }}>
              <div style={{ fontSize: 13, color: C.mutedText, fontWeight: 600, marginBottom: 6 }}>👨‍👩‍👧 家人提醒您</div>
              <div style={{ fontSize: 18, lineHeight: 1.8, fontWeight: 500 }}>"{result.advice}"</div>
            </div>
          )}

          {result.action && (
            <InfoCard icon="📋" label="建议您现在做" text={result.action} color={C.blueLight} textColor={C.blueWarm} labelColor={C.blueWarm} />
          )}

          <ResetBtn onClick={reset} label="↩ 再查验一条消息" />
        </div>
      )}

      {phase === "error" && (
        <div>
          <div style={{ background: C.redLight, borderRadius: 18, padding: "20px 22px" }}>
            <div style={{ fontSize: 17, color: C.redWarm, lineHeight: 1.6 }}>查验失败：{err}<br />请稍后再试。</div>
          </div>
          <ResetBtn onClick={reset} />
        </div>
      )}
    </div>
  );
}

// ─── MODULE 3: DIGITAL GUIDE ──────────────────────────────────────────────────

const QUICK_QUESTIONS = [
  "怎么用微信发红包？",
  "怎么用支付宝扫码付钱？",
  "怎么在手机上预约挂号？",
  "怎么叫网约车（滴滴）？",
  "怎么视频通话？",
  "怎么把照片发给家人？",
];

async function askGuide(question) {
  const sys = `你是专门帮助老年人学会使用智能手机的耐心教练。
说话方式：像对自己奶奶说话一样温柔，步骤清晰，绝对不用"点击""配置""刷新"等术语。
用"按""找""看到""点那个"等更直觉的词语。每步操作要非常具体，配合方位描述（左上角、中间大按钮等）。
返回JSON（不含代码块标记）：
{"title":"简短回答标题","steps":["第一步：…","第二步：…","第三步：…"],"tip":"一个小提示或注意事项","encourage":"一句鼓励的话"}`;
  const res = await fetch("https://api.anthropic.com/v1/messages", {
    method: "POST", headers: { "Content-Type": "application/json" },
    body: JSON.stringify({
      model: "claude-sonnet-4-20250514", max_tokens: 800, system: sys,
      messages: [{ role: "user", content: question }]
    })
  });
  if (!res.ok) throw new Error(`请求失败 ${res.status}`);
  const d = await res.json();
  return JSON.parse(d.content.map(b => b.text || "").join("").replace(/```json|```/g, "").trim());
}

function GuideModule({ onBack }) {
  const [question, setQuestion] = useState("");
  const [phase, setPhase] = useState("input");
  const [result, setResult] = useState(null);
  const [err, setErr] = useState(null);

  const ask = async (q) => {
    const finalQ = q || question;
    if (!finalQ.trim()) return;
    setQuestion(finalQ);
    setPhase("loading");
    try { setResult(await askGuide(finalQ)); setPhase("result"); }
    catch (e) { setErr(e.message); setPhase("error"); }
  };

  const reset = () => { setPhase("input"); setQuestion(""); setResult(null); setErr(null); };

  return (
    <div style={BASE.page}>
      <BackBtn onBack={onBack} />
      <div style={{ textAlign: "center", marginBottom: 32 }}>
        <div style={{ fontSize: 48 }}>📱</div>
        <div style={{ fontSize: 28, fontWeight: 800, marginTop: 8 }}>手机操作指南</div>
        <div style={{ fontSize: 16, color: C.mutedText, marginTop: 6, lineHeight: 1.6 }}>
          不会用手机某个功能？<br />用大白话问，AI 一步步教您
        </div>
      </div>

      {phase === "input" && (
        <div>
          <div style={{ background: "rgba(255,255,255,0.65)", borderRadius: 24, padding: 20, backdropFilter: "blur(8px)", marginBottom: 16 }}>
            <div style={{ fontSize: 16, color: C.mutedText, marginBottom: 10, fontWeight: 600 }}>您想学什么？直接问 👇</div>
            <textarea
              value={question} onChange={e => setQuestion(e.target.value)}
              placeholder="例如：&quot;怎么用微信发红包？&quot;"
              style={{
                width: "100%", minHeight: 100, fontSize: 18, lineHeight: 1.7,
                border: `1.5px solid ${C.stone}60`, borderRadius: 16, padding: "14px 16px",
                fontFamily: FONT, color: C.warmText, background: "rgba(255,255,255,0.8)",
                resize: "none", boxSizing: "border-box",
              }}
            />
            <button onClick={() => ask()} disabled={!question.trim()} style={{
              width: "100%", marginTop: 12, background: question.trim() ? C.blueWarm : C.stone,
              color: "#fff", border: "none", borderRadius: 50, padding: "18px 0",
              fontSize: 21, fontWeight: 700, cursor: question.trim() ? "pointer" : "default",
              fontFamily: FONT, transition: "background 0.2s",
            }}>📖 &nbsp;告诉我怎么做</button>
          </div>

          <div style={{ fontSize: 14, color: C.mutedText, marginBottom: 10, paddingLeft: 4, fontWeight: 600 }}>常见问题，点一下就能问</div>
          <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10 }}>
            {QUICK_QUESTIONS.map((q, i) => (
              <div key={i} onClick={() => ask(q)} style={{
                background: "rgba(255,255,255,0.6)", border: `1px solid ${C.stone}40`,
                borderRadius: 16, padding: "14px 14px", cursor: "pointer",
                fontSize: 16, color: C.warmText, lineHeight: 1.5, fontWeight: 500,
                textAlign: "center",
              }}>{q}</div>
            ))}
          </div>
        </div>
      )}

      {phase === "loading" && (
        <div style={{ textAlign: "center", padding: "60px 0" }}>
          <div style={{ fontSize: 56 }}>📖</div>
          <Dots />
          <div style={{ fontSize: 20, color: C.mutedText }}>正在准备教程…<br /><span style={{ fontSize: 16 }}>马上就好</span></div>
        </div>
      )}

      {phase === "result" && result && (
        <div>
          <div style={{ background: C.blueLight, borderRadius: 22, padding: "20px 22px", marginBottom: 16, border: `1.5px solid ${C.blueWarm}30` }}>
            <div style={{ fontSize: 13, color: C.blueWarm, fontWeight: 700, marginBottom: 4 }}>📱 {question}</div>
            <div style={{ fontSize: 24, fontWeight: 800, color: C.blueWarm }}>{result.title}</div>
          </div>

          <div style={{ background: "rgba(255,255,255,0.68)", borderRadius: 22, padding: "20px 22px", backdropFilter: "blur(8px)", marginBottom: 14 }}>
            <div style={{ fontSize: 15, color: C.mutedText, fontWeight: 700, marginBottom: 14 }}>一步一步来，不着急 👇</div>
            {result.steps?.map((s, i) => (
              <div key={i} style={{ display: "flex", gap: 14, alignItems: "flex-start", marginBottom: 16 }}>
                <div style={{
                  width: 36, height: 36, borderRadius: "50%", background: C.blueWarm,
                  color: "#fff", display: "flex", alignItems: "center", justifyContent: "center",
                  fontSize: 16, fontWeight: 800, flexShrink: 0,
                }}>{i + 1}</div>
                <div style={{ fontSize: 18, lineHeight: 1.7, color: C.warmText, paddingTop: 6 }}>{s.replace(/^第.步[：:]?\s*/,"")}</div>
              </div>
            ))}
          </div>

          {result.tip && <InfoCard icon="💡" label="小提示" text={result.tip} color={C.accentLight} />}

          {result.encourage && (
            <div style={{ background: `linear-gradient(135deg, ${C.linen}, ${C.cream})`, borderRadius: 20, padding: "16px 20px", border: `1.5px solid ${C.stone}40`, textAlign: "center" }}>
              <div style={{ fontSize: 18, lineHeight: 1.7, fontWeight: 500 }}>🌟 &nbsp;{result.encourage}</div>
            </div>
          )}

          <ResetBtn onClick={reset} label="↩ 再问一个问题" />
        </div>
      )}

      {phase === "error" && (
        <div>
          <div style={{ background: C.redLight, borderRadius: 18, padding: "20px 22px" }}>
            <div style={{ fontSize: 17, color: C.redWarm, lineHeight: 1.6 }}>出错了：{err}</div>
          </div>
          <ResetBtn onClick={reset} />
        </div>
      )}
    </div>
  );
}

// ─── ROOT ─────────────────────────────────────────────────────────────────────

export default function App() {
  const [page, setPage] = useState("home");
  return (
    <div style={BASE.app}>
      <style>{`
        @keyframes pulse { 0%,80%,100%{transform:scale(0.7);opacity:0.4} 40%{transform:scale(1.1);opacity:1} }
        @keyframes fadeUp { from{opacity:0;transform:translateY(18px)} to{opacity:1;transform:translateY(0)} }
        * { box-sizing: border-box; }
        button { font-family: ${FONT}; }
        textarea:focus, input:focus { outline: 2px solid ${C.accent}80; }
      `}</style>
      <div style={BASE.grain} />
      {page === "home"  && <Home onNav={setPage} />}
      {page === "meds"  && <MedsModule  onBack={() => setPage("home")} />}
      {page === "fraud" && <FraudModule onBack={() => setPage("home")} />}
      {page === "guide" && <GuideModule onBack={() => setPage("home")} />}
    </div>
  );
}
