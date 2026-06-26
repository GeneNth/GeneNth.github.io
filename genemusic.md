---
layout: default
title: GeneMusic Lab
permalink: /genemusic/
---

&lt;div class="about-card" markdown="1"&gt;

## 🎵 GeneMusic Lab

**探索基因与音乐的科学交叉领域**

&gt; *"DNA 是生命的乐谱，蛋白质是演奏的乐章。"*

&lt;/div&gt;

&lt;div class="about-card" markdown="1"&gt;

## 🧬 研究方向

| 领域 | 内容 |
|------|------|
| **基因表达谱分析** | 将 RNA-seq 数据转化为可听化的音高与节奏 |
| **蛋白质结构音乐化** | 把氨基酸序列映射为旋律与和声 |
| **DNA 序列作曲** | 基于 ATCG 碱基对生成算法音乐 |
| **生物节律研究** | 昼夜节律基因与音乐节拍的关联探索 |

&lt;/div&gt;

&lt;div class="about-card music-card" markdown="1"&gt;

## 🎼 Circadian Symphony

&lt;div class="music-player"&gt;
  &lt;audio id="audio1" src="{{ '/assets/music/circadian_symphony.mp3' | relative_url }}"&gt;&lt;/audio&gt;
  
  &lt;div class="player-main"&gt;
    &lt;button class="play-btn" onclick="togglePlay('audio1', this)"&gt;
      &lt;span class="play-icon"&gt;▶&lt;/span&gt;
      &lt;span class="pause-icon" style="display:none"&gt;⏸&lt;/span&gt;
    &lt;/button&gt;
    
    &lt;div class="player-info"&gt;
      &lt;div class="music-title"&gt;Circadian Symphony&lt;/div&gt;
      &lt;div class="music-meta"&gt;基于 CLOCK/BMAL1 基因表达数据 | 时长 03:24&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
  
  &lt;div class="progress-bar" onclick="seek(event, 'audio1')"&gt;
    &lt;div class="progress-fill" id="progress1"&gt;&lt;/div&gt;
  &lt;/div&gt;
  
  &lt;div class="time-display"&gt;
    &lt;span id="current1"&gt;00:00&lt;/span&gt; / &lt;span id="duration1"&gt;03:24&lt;/span&gt;
  &lt;/div&gt;
&lt;/div&gt;

&lt;div class="music-desc"&gt;

### 创作背景

这首作品基于**昼夜节律基因 CLOCK 和 BMAL1** 的 RNA-seq 表达数据创作。

**数据来源**：小鼠肝脏组织 24 小时周期性采样  
**算法**：Python Magenta + 自定义映射规则  
**映射逻辑**：
- 基因表达量 → 音高（高表达 = 高音）
- 表达变化率 → 节奏速度
- 周期性波动 → 和弦进行

**科学意义**：将不可见的基因调控网络转化为可听化的声音景观，帮助研究者直观感受生物钟的"分子节拍"。

&lt;/div&gt;

&lt;/div&gt;

&lt;div class="about-card music-card" markdown="1"&gt;

## 🎹 Protein Piano

&lt;div class="music-player"&gt;
  &lt;audio id="audio2" src="{{ '/assets/music/protein_piano.mp3' | relative_url }}"&gt;&lt;/audio&gt;
  
  &lt;div class="player-main"&gt;
    &lt;button class="play-btn" onclick="togglePlay('audio2', this)"&gt;
      &lt;span class="play-icon"&gt;▶&lt;/span&gt;
      &lt;span class="pause-icon" style="display:none"&gt;⏸&lt;/span&gt;
    &lt;/button&gt;
    
    &lt;div class="player-info"&gt;
      &lt;div class="music-title"&gt;Protein Piano&lt;/div&gt;
      &lt;div class="music-meta"&gt;α-螺旋与β-折叠结构映射 | 时长 02:15&lt;/div&gt;
    &lt;/div&gt;
  &lt;/div&gt;
  
  &lt;div class="progress-bar" onclick="seek(event, 'audio2')"&gt;
    &lt;div class="progress-fill" id="progress2"&gt;&lt;/div&gt;
  &lt;/div&gt;
  
  &lt;div class="time-display"&gt;
    &lt;span id="current2"&gt;00:00&lt;/span&gt; / &lt;span id="duration2"&gt;02:15&lt;/span&gt;
  &lt;/div&gt;
&lt;/div&gt;

&lt;div class="music-desc"&gt;

### 创作背景

将**蛋白质二级结构**映射为钢琴音色：

| 结构 | 音色映射 |
|------|----------|
| α-螺旋 | 温暖圆润的弦乐音色 |
| β-折叠 | 清脆明亮的钢琴高音 |
| 无规卷曲 | 环境音效铺垫 |

**数据来源**：PDB 数据库血红蛋白结构  
**算法**：Music21 + 自定义音色映射表

&lt;/div&gt;

&lt;/div&gt;

&lt;div class="about-card" markdown="1"&gt;

## 🎼 更多实验项目

- **Genome Jazz** — 用基因组变异数据即兴生成爵士乐段
- **Methyl-Beats** — 基于 DNA 甲基化模式的电子节奏
- **CRISPR Chords** — gRNA 序列与和弦进行的映射探索

&lt;/div&gt;

&lt;div class="about-card" markdown="1"&gt;

## 🔬 技术栈

&lt;span class="skill-tag"&gt;🎹 MIDI 编程&lt;/span&gt; &lt;span class="skill-tag"&gt;🐍 Python&lt;/span&gt; &lt;span class="skill-tag"&gt;📊 RNA-seq 分析&lt;/span&gt; &lt;span class="skill-tag"&gt;🎧 音频合成&lt;/span&gt;

&lt;/div&gt;

&lt;div class="about-card" markdown="1"&gt;

&gt; 🚧 **实验室建设中...**

*Coming soon.* 🎶

&lt;/div&gt;

&lt;script&gt;
function togglePlay(audioId, btn) {
  const audio = document.getElementById(audioId);
  const playIcon = btn.querySelector('.play-icon');
  const pauseIcon = btn.querySelector('.pause-icon');
  
  if (audio.paused) {
    // 暂停其他音频
    document.querySelectorAll('audio').forEach(a =&gt; {
      if (a.id !== audioId) {
        a.pause();
        a.currentTime = 0;
      }
    });
    // 重置其他按钮
    document.querySelectorAll('.play-btn').forEach(b =&gt; {
      if (b !== btn) {
        b.querySelector('.play-icon').style.display = '';
        b.querySelector('.pause-icon').style.display = 'none';
      }
    });
    
    audio.play();
    playIcon.style.display = 'none';
    pauseIcon.style.display = '';
  } else {
    audio.pause();
    playIcon.style.display = '';
    pauseIcon.style.display = 'none';
  }
}

// 进度条更新
document.querySelectorAll('audio').forEach(audio =&gt; {
  const id = audio.id.replace('audio', '');
  
  audio.addEventListener('timeupdate', () =&gt; {
    const progress = (audio.currentTime / audio.duration) * 100;
    document.getElementById('progress' + id).style.width = progress + '%';
    document.getElementById('current' + id).textContent = formatTime(audio.currentTime);
  });
  
  audio.addEventListener('loadedmetadata', () =&gt; {
    document.getElementById('duration' + id).textContent = formatTime(audio.duration);
  });
  
  audio.addEventListener('ended', () =&gt; {
    const btn = document.querySelector(`button[onclick*="${audio.id}"]`);
    btn.querySelector('.play-icon').style.display = '';
    btn.querySelector('.pause-icon').style.display = 'none';
  });
});

function seek(event, audioId) {
  const audio = document.getElementById(audioId);
  const bar = event.currentTarget;
  const clickX = event.offsetX;
  const width = bar.offsetWidth;
  const percent = clickX / width;
  audio.currentTime = percent * audio.duration;
}

function formatTime(seconds) {
  if (isNaN(seconds)) return '00:00';
  const mins = Math.floor(seconds / 60);
  const secs = Math.floor(seconds % 60);
  return String(mins).padStart(2, '0') + ':' + String(secs).padStart(2, '0');
}
&lt;/script&gt;
