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

&lt;/div&gt;

&lt;div class="about-card music-card"&gt;

## 🎹 Protein Piano

{% include music-player.html id="1" src="/assets/music/protein_piano.mp3" title="Protein Piano" meta="α-螺旋与β-折叠结构映射 | 时长 02:15" duration="02:15" %}

&lt;div class="music-desc" markdown="1"&gt;

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

- **Circadian Symphony** — 基于 CLOCK/BMAL1 基因表达数据的实时生成音乐
- **Genome Jazz** — 用基因组变异数据即兴生成爵士乐段
- **Methyl-Beats** — 基于 DNA 甲基化模式的电子节奏

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
    document.querySelectorAll('audio').forEach(a =&gt; {
      if (a.id !== audioId) { a.pause(); a.currentTime = 0; }
    });
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
  const percent = event.offsetX / bar.offsetWidth;
  audio.currentTime = percent * audio.duration;
}

function formatTime(seconds) {
  if (isNaN(seconds)) return '00:00';
  const m = Math.floor(seconds / 60);
  const s = Math.floor(seconds % 60);
  return String(m).padStart(2, '0') + ':' + String(s).padStart(2, '0');
}
&lt;/script&gt;
