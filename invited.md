---
layout: default
title: "Invited Speakers"
permalink: /invited/
---
<!-- 极简标题栏（完全复用原有样式） -->
<div class="simple-header">
  <h1>Invited Speakers</h1>
  <br/>
  <button id="sortByNameBtn" class="btn btn-primary" style="border: none;">
    Sort by Name
  </button>
  <button id="sortByScheduleBtn" class="btn btn-secondary" style="border: none;">
    Sort by Time Order
  </button>
</div>

<!-- 引导语 -->
<p>We are honored to invite the following researchers to present 16 talks:</p>

<!-- 讲者卡片容器（动态渲染） -->
<div id="speakersContainer" class="speakers-grid">
  <!-- 讲者卡片将通过JS动态生成 -->
</div>

<div class="alert alert-info mt-4" role="alert">
  If you have suggestions for invited talks aligned with the workshop scope, please reach out via the <a href="{{ '/contact/' | relative_url }}" style="color: var(--primary-color); font-weight: 500;">contact page</a>.
</div>

<!-- 新增：排序逻辑脚本 -->
<script>
// 1. 定义所有讲者数据（包含演讲时间段+排序序号）
const speakersData = [
  {
    name: "Ritam Bhaumik",
    affiliation: "Technology Innovation Institute, Abu Dhabi, UAE",
    talkTitle: "Post-Quantum Security of Key-Alternating Feistel Ciphers and other Symmetric Modes",
    keywords: ["post-quantum", "Q1", "Feistel", "provable security", "resampling"],
    speechOrder: 15, // 仅用于排序
    timeSlot: "Mar 21, 11:00 - 11:30" // 具体时间段
  },
  {
    name: "Wonseok Choi",
    affiliation: "DGIST",
    talkTitle: "On Reduced Key Spaces of Even–Mansour Ciphers",
    keywords: ["Symmetric-key cryptography", "provable security", "Even-Mansour cipher", "public permutations", "key scheduling"],
    speechOrder: 12,
    timeSlot: "Mar 21, 09:00 - 09:30"
  },
  {
    name: "Antonio Florez-Gutierrez",
    affiliation: "NTT Social Informatics Laboratories",
    talkTitle: "Puncturing Linear Key Recovery Attacks",
    keywords: ["linear cryptanalysis", "puncturing"],
    speechOrder: 2,
    timeSlot: "Mar 19, 10:00 - 10:30",
    slides: "/assets/slides/Antonio Florez-Gutierrez.pdf"
  },
  {
    name: "Jonathan Fuchs",
    affiliation: "Radboud University",
    talkTitle: "On the Equivalence of Forgery and Key Recovery in Key-Then-Hash Functions",
    keywords: ["message authentication codes", "key recovery", "key-then-hash", "offset-invariance", "NH"],
    speechOrder: 3,
    timeSlot: "Mar 19, 11:00 - 11:30"
  },
  {
    name: "Tao Huang",
    affiliation: "Huawei International Pte. Ltd.",
    talkTitle: "Scenario-Oriented High-Throughput Cipher Design",
    keywords: ["High-Throughput", "Encryption", "Stream Cipher"],
    speechOrder: 5,
    timeSlot: "Mar 19, 12:00 - 12:30"
  },
  {
    name: "Ashwin Jha",
    affiliation: "Ruhr University Bochum, Germany",
    talkTitle: "Constrained Systems",
    keywords: ["PRF Security", "1k-PMAC+", "1k-LightMAC+", "Sum of Even-Mansour"],
    speechOrder: 4,
    timeSlot: "Mar 19, 11:30 - 12:00",
    slides: "/assets/slides/Ashwin Jha.pdf"
  },
  {
    name: "Tetsu Iwata",
    affiliation: "Nagoya University",
    talkTitle: "Committing Security of GCM and Related AEAD",
    keywords: ["Committing security", "GCM", "AEAD"],
    speechOrder: 14,
    timeSlot: "Mar 21, 10:00 - 10:30"
  },
  {
    name: "Gregor Leander",
    affiliation: "Ruhr University Bochum",
    talkTitle: "Attacks and Remedies for Randomness in generative AI",
    keywords: ["PRNGs", "AI"],
    speechOrder: 1,
    timeSlot: "Mar 19, 09:30 - 10:00"
  },
  {
    name: "Gaëtan Leurent",
    affiliation: "INRIA Paris",
    talkTitle: "Cryptanalysis of Algebraic Verifiable Delay Functions",
    keywords: ["Cryptanalysis", "VDF"],
    speechOrder: 13,
    timeSlot: "Mar 21, 09:30 - 10:00"
  },
  {
    name: "Meicheng Liu",
    affiliation: "Institute of Information Engineering, Chinese Academy of Sciences, China",
    talkTitle: "Security Analysis of the SHA-3 Hash Function",
    keywords: ["SHA-3", "Collision", "Preimage", "Hash Function"],
    speechOrder: 6,
    timeSlot: "Mar 20, 09:00 - 09:30",
    slides: "/assets/slides/Meicheng Liu.pdf"
  },
  {
    name: "Kazuhiko Minematsu",
    affiliation: "NEC",
    talkTitle: "Do not Mix Models: Revisiting Generic Transforms for Committing Authenticated Encryption",
    keywords: ["Committing Authenticated Encryption", "Generic Transform", "Idealized Model"],
    speechOrder: 16,
    timeSlot: "Mar 21, 11:30 - 12:00",
    slides: "/assets/slides/Kazuhiko Minematsu.pdf"
  },
  {
    name: "Hrithik Nandi",
    affiliation: "IAI TCG CREST and RKMVERI, India",
    talkTitle: "Short-Input Random Oracle from Public Random Permutations",
    keywords: ["Indifferentiability", "RP-to-RF conversion", "Chaining attack"],
    speechOrder: 8,
    timeSlot: "Mar 20, 10:00 - 10:30",
    slides: "/assets/slides/Hrithik Nandi.pdf"
  },
  {
    name: "Patrick Neumann",
    affiliation: "Inria Paris",
    talkTitle: "Meet-in-the-Middle Attacks on Full ChiLow",
    keywords: ["Meet-in-the-Middle", "Key-Recovery Attack", "Symmetric Cryptanalysis", "ChiLow", "Key Dependencies", "State Dependencies"],
    speechOrder: 9,
    timeSlot: "Mar 20, 11:00 - 11:30",
    slides: "/assets/slides/Patrick Neumann.pdf"
  },
  {
    name: "Christian Rechberger",
    affiliation: "TU Graz and TACEO",
    talkTitle: "An update on MPC- and ZK-friendly symmetric crypto",
    keywords: ["ciphers", "hashing", "PRF", "OWF", "cryptanalysis", "SMPC", "ZK"],
    speechOrder: 10,
    timeSlot: "Mar 20, 11:30 - 12:00"
  },
  {
    name: "Yaobin Shen",
    affiliation: "Xiamen University",
    talkTitle: "Tight Generic PRF Security of HMAC and NMAC",
    keywords: ["HMAC", "NMAC", "generic security", "provable security"],
    speechOrder: 7,
    timeSlot: "Mar 20, 09:30 - 10:00",
    slides: "/assets/slides/Yaobin Shen.pdf"
  },
  {
    name: "Bin Zhang",
    affiliation: "Institute of Software, Chinese Academy of Sciences",
    talkTitle: "Vectorial Fast Correlation Attacks over Extension Fields",
    keywords: ["Stream ciphers", "Extension Fields", "SNOW"],
    speechOrder: 11,
    timeSlot: "Mar 20, 12:00 - 12:30",
    slides: "/assets/slides/Bin Zhang.pdf"
  }
];

// 2. 渲染讲者卡片的函数（核心修改：展示时间段而非数字）
function renderSpeakers(speakers) {
  const container = document.getElementById('speakersContainer');
  container.innerHTML = ''; // 清空原有内容
  
  speakers.forEach(speaker => {
    // 创建卡片元素
    const card = document.createElement('div');
    card.className = 'callout';
    
    // 构建卡片内容（替换Speech Order为Time Slot，展示具体时间段）
    card.innerHTML = `
      <div style="display: flex; align-items: center; justify-content: space-between; gap: 1rem; margin-bottom: 1rem;">
    <h3 style="margin: 0; flex-shrink: 1;">${speaker.name}</h3>
    ${speaker.slides ? `<a href="${speaker.slides}" target="_blank" class="btn btn-sm btn-primary">Slides</a>` : ''}
  </div>
      <p class="speaker-affiliation">${speaker.affiliation}</p>
      <p><span class="speaker-talk-label">Talk Title:</span> ${speaker.talkTitle}</p>
      <div class="speaker-keywords">
        ${speaker.keywords.map(keyword => `<span class="speaker-keyword">${keyword}</span>`).join('')}
      </div>
      ${speaker.timeSlot ? `<p style="margin-top:0.75rem; font-size:0.9rem; color:var(--text-muted);">
        <strong>Time Slot:</strong> ${speaker.timeSlot}
      </p>` : ''}
    `;
    
    container.appendChild(card);
  });
}

// 3. 排序函数（逻辑不变，仍按演讲时间顺序排序）
function sortSpeakersByName() {
  const sorted = [...speakersData].sort((a, b) => {
    return a.name.localeCompare(b.name);
  });
  renderSpeakers(sorted);
}

function sortSpeakersBySchedule() {
  const sorted = [...speakersData].sort((a, b) => {
    return a.speechOrder - b.speechOrder;
  });
  renderSpeakers(sorted);
}

// 4. 绑定按钮事件
document.getElementById('sortByNameBtn').addEventListener('click', () => {
  sortSpeakersByName();
  // 按钮样式切换
  document.getElementById('sortByNameBtn').classList.add('btn-primary');
  document.getElementById('sortByNameBtn').classList.remove('btn-secondary');
  document.getElementById('sortByScheduleBtn').classList.add('btn-secondary');
  document.getElementById('sortByScheduleBtn').classList.remove('btn-primary');
});

document.getElementById('sortByScheduleBtn').addEventListener('click', () => {
  sortSpeakersBySchedule();
  // 按钮样式切换
  document.getElementById('sortByScheduleBtn').classList.add('btn-primary');
  document.getElementById('sortByScheduleBtn').classList.remove('btn-secondary');
  document.getElementById('sortByNameBtn').classList.add('btn-secondary');
  document.getElementById('sortByNameBtn').classList.remove('btn-primary');
});

// 5. 页面加载时默认按姓氏排序
window.onload = sortSpeakersByName;
</script>