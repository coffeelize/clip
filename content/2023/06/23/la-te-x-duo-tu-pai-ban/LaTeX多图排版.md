---
title: "LaTeX 多图排版"
date: 2023-06-23T13:34:02+08:00
updated: 2023-06-23T13:34:02+08:00
taxonomies:
  tags: []
extra:
  source: https://coffeelize.top/posts/809da89d.html
  hostname: coffeelize.top
  author: 
  original_title: "LaTeX 多图排版"
  original_lang: zh-CN
---

### [](https://coffeelize.top/posts/809da89d.html#%E5%9B%BE%E7%89%87%E6%8E%92%E7%89%88 "图片排版")图片排版

-   搭配 [coffeelize.sty](https://coffeelize.top/posts/9165505d.html) 宏包使用
-   使用 subfigure 宏包

#### [](https://coffeelize.top/posts/809da89d.html#%E4%B8%A4%E5%9B%BE%E5%B9%B6%E6%8E%92 "两图并排")两图并排

<table><tbody><tr><td><pre><span>1</span><br><span>2</span><br><span>3</span><br><span>4</span><br><span>5</span><br><span>6</span><br><span>7</span><br><span>8</span><br><span>9</span><br><span>10</span><br><span>11</span><br><span>12</span><br><span>13</span><br><span>14</span><br><span>15</span><br><span>16</span><br><span>17</span><br><span>18</span><br><span>19</span><br><span>20</span><br></pre></td><td><pre><span>\documentclass{ctexart}</span><br><span>\usepackage{coffeelize}</span><br><span>\usepackage{graphicx}</span><br><span>\usepackage{subfigure}</span><br><span></span><br><span>\begin{document}</span><br><span></span><br><span>\begin{figure}[htbp]</span><br><span> \centering</span><br><span> \subfigure[subfig:1]{</span><br><span>  \includegraphics[width=0.48\textwidth]{example-image-A}</span><br><span> }</span><br><span> \subfigure[subfig:2]{</span><br><span>  \includegraphics[width=0.48\textwidth]{example-image-A}</span><br><span> }</span><br><span> \caption{两张图片并列}</span><br><span> \label{fig:subfigure_example1}</span><br><span>\end{figure}</span><br><span> </span><br><span>\end{document}</span><br></pre></td></tr></tbody></table>

![01-两图并排.png](Sp3heqlWH25wGia.png)

#### [](https://coffeelize.top/posts/809da89d.html#%E4%B8%89%E5%9B%BE%E5%B9%B6%E6%8E%92 "三图并排")三图并排

<table><tbody><tr><td><pre><span>1</span><br><span>2</span><br><span>3</span><br><span>4</span><br><span>5</span><br><span>6</span><br><span>7</span><br><span>8</span><br><span>9</span><br><span>10</span><br><span>11</span><br><span>12</span><br><span>13</span><br><span>14</span><br><span>15</span><br><span>16</span><br><span>17</span><br><span>18</span><br><span>19</span><br><span>20</span><br><span>21</span><br><span>22</span><br><span>23</span><br></pre></td><td><pre><span>\documentclass{ctexart}</span><br><span>\usepackage{coffeelize}</span><br><span>\usepackage{graphicx}</span><br><span>\usepackage{subfigure}</span><br><span></span><br><span>\begin{document}</span><br><span></span><br><span>\begin{figure}[htbp]</span><br><span> \centering</span><br><span> \subfigure[subfig:1]{</span><br><span>  \includegraphics[width=0.3\textwidth]{example-image-A}</span><br><span> }</span><br><span> \subfigure[subfig:2]{</span><br><span>  \includegraphics[width=0.3\textwidth]{example-image-A}</span><br><span> }</span><br><span> \subfigure[subfig:3]{</span><br><span> \includegraphics[width=0.3\textwidth]{example-image-A}</span><br><span> }</span><br><span> \caption{两张图片并列}</span><br><span> \label{fig:subfigure_example1}</span><br><span>\end{figure}</span><br><span> </span><br><span>\end{document}</span><br></pre></td></tr></tbody></table>

![02-三图并排.png](KtFlv43dJy2Ppui.png)

#### [](https://coffeelize.top/posts/809da89d.html#%E5%9B%9B%E5%9B%BE%E5%B9%B6%E6%8E%92 "四图并排")四图并排

<table><tbody><tr><td><pre><span>1</span><br><span>2</span><br><span>3</span><br><span>4</span><br><span>5</span><br><span>6</span><br><span>7</span><br><span>8</span><br><span>9</span><br><span>10</span><br><span>11</span><br><span>12</span><br><span>13</span><br><span>14</span><br><span>15</span><br><span>16</span><br><span>17</span><br><span>18</span><br><span>19</span><br><span>20</span><br><span>21</span><br><span>22</span><br><span>23</span><br><span>24</span><br><span>25</span><br><span>26</span><br></pre></td><td><pre><span>\documentclass{ctexart}</span><br><span>\usepackage{coffeelize}</span><br><span>\usepackage{graphicx}</span><br><span>\usepackage{subfigure}</span><br><span></span><br><span>\begin{document}</span><br><span></span><br><span>\begin{figure}[htbp]</span><br><span> \centering</span><br><span> \subfigure[subfig:1]{</span><br><span>  \includegraphics[width=0.2\textwidth]{example-image-A}</span><br><span> }</span><br><span> \subfigure[subfig:2]{</span><br><span>  \includegraphics[width=0.2\textwidth]{example-image-A}</span><br><span> }</span><br><span> \subfigure[subfig:3]{</span><br><span> \includegraphics[width=0.2\textwidth]{example-image-A}</span><br><span> }</span><br><span> \subfigure[subfig:4]{</span><br><span> \includegraphics[width=0.2\textwidth]{example-image-A}</span><br><span> }</span><br><span> \caption{两张图片并列}</span><br><span> \label{fig:subfigure_example1}</span><br><span>\end{figure}</span><br><span> </span><br><span>\end{document}</span><br></pre></td></tr></tbody></table>

![03-四图并排.png](a5zSktW8C19GbYJ.png)

#### [](https://coffeelize.top/posts/809da89d.html#%E4%B8%A4%E8%A1%8C%E5%9B%9B%E5%9B%BE%E5%B9%B6%E6%8E%92 "两行四图并排")两行四图并排

<table><tbody><tr><td><pre><span>1</span><br><span>2</span><br><span>3</span><br><span>4</span><br><span>5</span><br><span>6</span><br><span>7</span><br><span>8</span><br><span>9</span><br><span>10</span><br><span>11</span><br><span>12</span><br><span>13</span><br><span>14</span><br><span>15</span><br><span>16</span><br><span>17</span><br><span>18</span><br><span>19</span><br></pre></td><td><pre><span>\documentclass{ctexart}</span><br><span>\usepackage{coffeelize}</span><br><span>\usepackage{graphicx}</span><br><span>\usepackage{subfigure}</span><br><span></span><br><span>\begin{document}</span><br><span></span><br><span>\begin{figure}[htbp]</span><br><span> \centering</span><br><span> \subfigure[图1]{\includegraphics[width=0.48\linewidth]{example-image-A}}\quad</span><br><span> \subfigure[图2]{\includegraphics[width=0.48\linewidth]{example-image-A}}</span><br><span> \\</span><br><span> \subfigure[图3]{\includegraphics[width=0.48\linewidth]{example-image-A}}\quad</span><br><span> \subfigure[图4]{\includegraphics[width=0.48\linewidth]{example-image-A}}</span><br><span> \caption{两列并排的四张小图}</span><br><span> \label{fig:subfigure_example4}</span><br><span>\end{figure}</span><br><span> </span><br><span>\end{document}</span><br></pre></td></tr></tbody></table>

![04-两行四图并排.png](Q9vjLKRUynJDbXI.png)

#### [](https://coffeelize.top/posts/809da89d.html#%E4%B8%A4%E8%A1%8C%E5%85%AD%E5%9B%BE%E5%B9%B6%E6%8E%92 "两行六图并排")两行六图并排

<table><tbody><tr><td><pre><span>1</span><br><span>2</span><br><span>3</span><br><span>4</span><br><span>5</span><br><span>6</span><br><span>7</span><br><span>8</span><br><span>9</span><br><span>10</span><br><span>11</span><br><span>12</span><br><span>13</span><br><span>14</span><br><span>15</span><br><span>16</span><br><span>17</span><br><span>18</span><br><span>19</span><br><span>20</span><br><span>21</span><br></pre></td><td><pre><span>\documentclass{ctexart}</span><br><span>\usepackage{coffeelize}</span><br><span>\usepackage{graphicx}</span><br><span>\usepackage{subfigure}</span><br><span></span><br><span>\begin{document}</span><br><span></span><br><span>\begin{figure}[htbp]</span><br><span> \centering</span><br><span> \subfigure[图1]{\includegraphics[width=0.3\linewidth]{example-image-A}}\quad</span><br><span> \subfigure[图2]{\includegraphics[width=0.3\linewidth]{example-image-A}}\quad</span><br><span> \subfigure[图3]{\includegraphics[width=0.3\linewidth]{example-image-A}}</span><br><span> \\</span><br><span> \subfigure[图4]{\includegraphics[width=0.3\linewidth]{example-image-A}}\quad</span><br><span> \subfigure[图5]{\includegraphics[width=0.3\linewidth]{example-image-A}}\quad</span><br><span> \subfigure[图6]{\includegraphics[width=0.3\linewidth]{example-image-A}}</span><br><span> \caption{两列并排的六张小图}</span><br><span> \label{fig:subfigure_example4}</span><br><span>\end{figure}</span><br><span> </span><br><span>\end{document}</span><br></pre></td></tr></tbody></table>

![05-两行六图并排.png](awT4oAp6u3C21kx.png)
