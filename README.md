<div align="center">

<!-- 超大总星数徽章 -->
<a href="https://github.com/sodous-s?tab=repositories">
  <img src="https://img.shields.io/github/stars/sodous-s?label=Total%20Stars&style=for-the-badge&logo=github&color=blueviolet&labelColor=000000&logoColor=white" height="70">
</a>

<!-- 多语言标题 -->
<h1>自我介绍 | Self-Introduction | Selbstvorstellung | Présentation | Memprezento | 吾之自述</h1>

<!-- 语言选择链接 -->
<div style="margin: 20px 0; font-size: 18px;">
  <a href="#chinese">中文</a> | 
  <a href="#english">English</a> | 
  <a href="#german">Deutsch</a> | 
  <a href="#french">Français</a> |
  <a href="#esperanto">Esperanto</a> | 
  <a href="#classical">文言文</a>
</div>

</div>

<!-- 英文自我介绍 (默认显示) -->
<div id="english">
  <h2 align="center">👨 About Me</h2>
  
  <p align="center">
    [在此处添加您的英文自我介绍]
  </p>
  
  <h3 align="center">🛠 Tech Stack</h3>
  <p align="center">
    [在此处添加您的技术栈]
  </p>
  
  <h3 align="center">🌟 Featured Projects</h3>
  <p align="center">
    [在此处添加您的项目]
  </p>
</div>

<!-- 中文自我介绍 -->
<div id="chinese" style="display:none;">
  <h2 align="center">🧑 自我介绍</h2>
  
  <p align="center">
    [在此处添加您的中文自我介绍]
  </p>
  
  <h3 align="center">🛠 技术栈</h3>
  <p align="center">
    [在此处添加您的技术栈]
  </p>
  
  <h3 align="center">🌟 精选项目</h3>
  <p align="center">
    [在此处添加您的项目]
  </p>
</div>

<!-- 德语自我介绍 -->
<div id="german" style="display:none;">
  <h2 align="center">👨 Über Mich</h2>
  
  <p align="center">
    [在此处添加您的德语自我介绍]
  </p>
  
  <h3 align="center">🛠 Technologie-Stack</h3>
  <p align="center">
    [在此处添加您的技术栈]
  </p>
  
  <h3 align="center">🌟 Ausgewählte Projekte</h3>
  <p align="center">
    [在此处添加您的项目]
  </p>
</div>

<!-- 法语自我介绍 -->
<div id="french" style="display:none;">
  <h2 align="center">👨 Présentation</h2>
  
  <p align="center">
    [在此处添加您的法语自我介绍]
  </p>
  
  <h3 align="center">🛠 Stack Technologique</h3>
  <p align="center">
    [在此处添加您的技术栈]
  </p>
  
  <h3 align="center">🌟 Projets Sélectionnés</h3>
  <p align="center">
    [在此处添加您的项目]
  </p>
</div>

<!-- 世界语自我介绍 -->
<div id="esperanto" style="display:none;">
  <h2 align="center">👨 Pri Mi</h2>
  
  <p align="center">
    [在此处添加您的世界语自我介绍]
  </p>
  
  <h3 align="center">🛠 Teknologia Stako</h3>
  <p align="center">
    [在此处添加您的技术栈]
  </p>
  
  <h3 align="center">🌟 Elektitaj Projektoj</h3>
  <p align="center">
    [在此处添加您的项目]
  </p>
</div>

<!-- 文言文自我介绍 -->
<div id="classical" style="display:none;">
  <h2 align="center">👨 吾之自述</h2>
  
  <p align="center">
    [在此处添加您的文言文自我介绍]
  </p>
  
  <h3 align="center">🛠 技艺</h3>
  <p align="center">
    [在此处添加您的技术栈]
  </p>
  
  <h3 align="center">🌟 得意之作</h3>
  <p align="center">
    [在此处添加您的项目]
  </p>
</div>

<!-- 语言切换脚本 -->
<script>
// 获取URL中的语言参数
const urlParams = new URLSearchParams(window.location.search);
const lang = urlParams.get('lang');

// 显示对应语言的内容
function showLanguage(language) {
  // 隐藏所有语言部分
  document.querySelectorAll('div[id]').forEach(div => {
    if (div.id !== 'english' && div.id !== 'chinese' && 
        div.id !== 'german' && div.id !== 'french' &&
        div.id !== 'esperanto' && div.id !== 'classical') return;
    div.style.display = 'none';
  });
  
  // 显示选中的语言
  if (document.getElementById(language)) {
    document.getElementById(language).style.display = 'block';
  } else {
    document.getElementById('english').style.display = 'block';
  }
  
  // 更新URL参数
  window.history.replaceState({}, '', `${window.location.pathname}?lang=${language}`);
}

// 页面加载时根据URL参数显示对应语言
window.onload = function() {
  if (lang) {
    showLanguage(lang);
  } else {
    showLanguage('english');
  }
  
  // 为语言链接添加点击事件
  document.querySelectorAll('a[href^="#"]').forEach(link => {
    link.addEventListener('click', function(e) {
      e.preventDefault();
      const langId = this.getAttribute('href').substring(1);
      showLanguage(langId);
    });
  });
}
</script>
