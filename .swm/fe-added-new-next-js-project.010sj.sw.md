---
id: 010sj
title: "FE: added new next js project"
file_version: 1.1.2
app_version: 1.3.6
---

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/.eslintrc.json
```json
1      {
2        "extends": "next/core-web-vitals"
3      }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/.gitignore
```gitignore
1      # See https://help.github.com/articles/ignoring-files/ for more about ignoring files.
2      
3      # dependencies
4      /node_modules
5      /.pnp
6      .pnp.js
7      
8      # testing
9      /coverage
10     
11     # next.js
12     /.next/
13     /out/
14     
15     # production
16     /build
17     
18     # misc
19     .DS_Store
20     *.pem
21     
22     # debug
23     npm-debug.log*
24     yarn-debug.log*
25     yarn-error.log*
26     .pnpm-debug.log*
27     
28     # local env files
29     .env*.local
30     
31     # vercel
32     .vercel
33     
34     # typescript
35     *.tsbuildinfo
36     next-env.d.ts
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/README.md
```markdown
1      This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).
2      
3      ## Getting Started
4      
5      First, run the development server:
6      
7      ```bash
8      npm run dev
9      # or
10     yarn dev
11     # or
12     pnpm dev
13     ```
14     
15     Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
16     
17     You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.
18     
19     [API routes](https://nextjs.org/docs/api-routes/introduction) can be accessed on [http://localhost:3000/api/hello](http://localhost:3000/api/hello). This endpoint can be edited in `pages/api/hello.ts`.
20     
21     The `pages/api` directory is mapped to `/api/*`. Files in this directory are treated as [API routes](https://nextjs.org/docs/api-routes/introduction) instead of React pages.
22     
23     This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.
24     
25     ## Learn More
26     
27     To learn more about Next.js, take a look at the following resources:
28     
29     - [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
30     - [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.
31     
32     You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!
33     
34     ## Deploy on Vercel
35     
36     The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.
37     
38     Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/next.config.js
```javascript
1      /** @type {import('next').NextConfig} */
2      const nextConfig = {
3        experimental: {
4          appDir: true,
5        },
6      }
7      
8      module.exports = nextConfig
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/package.json
```json
1      {
2        "name": "new-next",
3        "version": "0.1.0",
4        "private": true,
5        "scripts": {
6          "dev": "next dev",
7          "build": "next build",
8          "start": "next start",
9          "lint": "next lint"
10       },
11       "dependencies": {
12         "@types/node": "18.14.3",
13         "@types/react": "18.0.28",
14         "@types/react-dom": "18.0.11",
15         "eslint": "8.35.0",
16         "eslint-config-next": "13.2.3",
17         "next": "13.2.3",
18         "react": "18.2.0",
19         "react-dom": "18.2.0",
20         "typescript": "4.9.5"
21       }
22     }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/src/app/api/hello/route.ts
```typescript
1      export async function GET(request: Request) {
2        return new Response('Hello, Next.js!')
3      }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/src/app/globals.css
```css
1      :root {
2        --max-width: 1100px;
3        --border-radius: 12px;
4        --font-mono: ui-monospace, Menlo, Monaco, 'Cascadia Mono', 'Segoe UI Mono',
5          'Roboto Mono', 'Oxygen Mono', 'Ubuntu Monospace', 'Source Code Pro',
6          'Fira Mono', 'Droid Sans Mono', 'Courier New', monospace;
7      
8        --foreground-rgb: 0, 0, 0;
9        --background-start-rgb: 214, 219, 220;
10       --background-end-rgb: 255, 255, 255;
11     
12       --primary-glow: conic-gradient(
13         from 180deg at 50% 50%,
14         #16abff33 0deg,
15         #0885ff33 55deg,
16         #54d6ff33 120deg,
17         #0071ff33 160deg,
18         transparent 360deg
19       );
20       --secondary-glow: radial-gradient(
21         rgba(255, 255, 255, 1),
22         rgba(255, 255, 255, 0)
23       );
24     
25       --tile-start-rgb: 239, 245, 249;
26       --tile-end-rgb: 228, 232, 233;
27       --tile-border: conic-gradient(
28         #00000080,
29         #00000040,
30         #00000030,
31         #00000020,
32         #00000010,
33         #00000010,
34         #00000080
35       );
36     
37       --callout-rgb: 238, 240, 241;
38       --callout-border-rgb: 172, 175, 176;
39       --card-rgb: 180, 185, 188;
40       --card-border-rgb: 131, 134, 135;
41     }
42     
43     @media (prefers-color-scheme: dark) {
44       :root {
45         --foreground-rgb: 255, 255, 255;
46         --background-start-rgb: 0, 0, 0;
47         --background-end-rgb: 0, 0, 0;
48     
49         --primary-glow: radial-gradient(rgba(1, 65, 255, 0.4), rgba(1, 65, 255, 0));
50         --secondary-glow: linear-gradient(
51           to bottom right,
52           rgba(1, 65, 255, 0),
53           rgba(1, 65, 255, 0),
54           rgba(1, 65, 255, 0.3)
55         );
56     
57         --tile-start-rgb: 2, 13, 46;
58         --tile-end-rgb: 2, 5, 19;
59         --tile-border: conic-gradient(
60           #ffffff80,
61           #ffffff40,
62           #ffffff30,
63           #ffffff20,
64           #ffffff10,
65           #ffffff10,
66           #ffffff80
67         );
68     
69         --callout-rgb: 20, 20, 20;
70         --callout-border-rgb: 108, 108, 108;
71         --card-rgb: 100, 100, 100;
72         --card-border-rgb: 200, 200, 200;
73       }
74     }
75     
76     * {
77       box-sizing: border-box;
78       padding: 0;
79       margin: 0;
80     }
81     
82     html,
83     body {
84       max-width: 100vw;
85       overflow-x: hidden;
86     }
87     
88     body {
89       color: rgb(var(--foreground-rgb));
90       background: linear-gradient(
91           to bottom,
92           transparent,
93           rgb(var(--background-end-rgb))
94         )
95         rgb(var(--background-start-rgb));
96     }
97     
98     a {
99       color: inherit;
100      text-decoration: none;
101    }
102    
103    @media (prefers-color-scheme: dark) {
104      html {
105        color-scheme: dark;
106      }
107    }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/src/app/layout.tsx
```tsx
1      import './globals.css'
2      
3      export const metadata = {
4        title: 'Create Next App',
5        description: 'Generated by create next app',
6      }
7      
8      export default function RootLayout({
9        children,
10     }: {
11       children: React.ReactNode
12     }) {
13       return (
14         <html lang="en">
15           <body>{children}</body>
16         </html>
17       )
18     }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/src/app/page.module.css
```css
1      .main {
2        display: flex;
3        flex-direction: column;
4        justify-content: space-between;
5        align-items: center;
6        padding: 6rem;
7        min-height: 100vh;
8      }
9      
10     .description {
11       display: inherit;
12       justify-content: inherit;
13       align-items: inherit;
14       font-size: 0.85rem;
15       max-width: var(--max-width);
16       width: 100%;
17       z-index: 2;
18       font-family: var(--font-mono);
19     }
20     
21     .description a {
22       display: flex;
23       align-items: center;
24       justify-content: center;
25       gap: 0.5rem;
26     }
27     
28     .description p {
29       position: relative;
30       margin: 0;
31       padding: 1rem;
32       background-color: rgba(var(--callout-rgb), 0.5);
33       border: 1px solid rgba(var(--callout-border-rgb), 0.3);
34       border-radius: var(--border-radius);
35     }
36     
37     .code {
38       font-weight: 700;
39       font-family: var(--font-mono);
40     }
41     
42     .grid {
43       display: grid;
44       grid-template-columns: repeat(3, minmax(33%, auto));
45       width: var(--max-width);
46       max-width: 100%;
47     }
48     
49     .card {
50       padding: 1rem 1.2rem;
51       border-radius: var(--border-radius);
52       background: rgba(var(--card-rgb), 0);
53       border: 1px solid rgba(var(--card-border-rgb), 0);
54       transition: background 200ms, border 200ms;
55     }
56     
57     .card span {
58       display: inline-block;
59       transition: transform 200ms;
60     }
61     
62     .card h2 {
63       font-weight: 600;
64       margin-bottom: 0.7rem;
65     }
66     
67     .card p {
68       margin: 0;
69       opacity: 0.6;
70       font-size: 0.9rem;
71       line-height: 1.5;
72       max-width: 34ch;
73     }
74     
75     .center {
76       display: flex;
77       justify-content: center;
78       align-items: center;
79       position: relative;
80       padding: 4rem 0;
81     }
82     
83     .center::before {
84       background: var(--secondary-glow);
85       border-radius: 50%;
86       width: 480px;
87       height: 360px;
88       margin-left: -400px;
89     }
90     
91     .center::after {
92       background: var(--primary-glow);
93       width: 240px;
94       height: 180px;
95       z-index: -1;
96     }
97     
98     .center::before,
99     .center::after {
100      content: '';
101      left: 50%;
102      position: absolute;
103      filter: blur(45px);
104      transform: translateZ(0);
105    }
106    
107    .logo,
108    .thirteen {
109      position: relative;
110    }
111    
112    .thirteen {
113      display: flex;
114      justify-content: center;
115      align-items: center;
116      width: 75px;
117      height: 75px;
118      padding: 25px 10px;
119      margin-left: 16px;
120      transform: translateZ(0);
121      border-radius: var(--border-radius);
122      overflow: hidden;
123      box-shadow: 0px 2px 8px -1px #0000001a;
124    }
125    
126    .thirteen::before,
127    .thirteen::after {
128      content: '';
129      position: absolute;
130      z-index: -1;
131    }
132    
133    /* Conic Gradient Animation */
134    .thirteen::before {
135      animation: 6s rotate linear infinite;
136      width: 200%;
137      height: 200%;
138      background: var(--tile-border);
139    }
140    
141    /* Inner Square */
142    .thirteen::after {
143      inset: 0;
144      padding: 1px;
145      border-radius: var(--border-radius);
146      background: linear-gradient(
147        to bottom right,
148        rgba(var(--tile-start-rgb), 1),
149        rgba(var(--tile-end-rgb), 1)
150      );
151      background-clip: content-box;
152    }
153    
154    /* Enable hover only on non-touch devices */
155    @media (hover: hover) and (pointer: fine) {
156      .card:hover {
157        background: rgba(var(--card-rgb), 0.1);
158        border: 1px solid rgba(var(--card-border-rgb), 0.15);
159      }
160    
161      .card:hover span {
162        transform: translateX(4px);
163      }
164    }
165    
166    @media (prefers-reduced-motion) {
167      .thirteen::before {
168        animation: none;
169      }
170    
171      .card:hover span {
172        transform: none;
173      }
174    }
175    
176    /* Mobile and Tablet */
177    @media (max-width: 1023px) {
178      .content {
179        padding: 4rem;
180      }
181    
182      .grid {
183        grid-template-columns: 1fr;
184        margin-bottom: 120px;
185        max-width: 320px;
186        text-align: center;
187      }
188    
189      .card {
190        padding: 1rem 2.5rem;
191      }
192    
193      .card h2 {
194        margin-bottom: 0.5rem;
195      }
196    
197      .center {
198        padding: 8rem 0 6rem;
199      }
200    
201      .center::before {
202        transform: none;
203        height: 300px;
204      }
205    
206      .description {
207        font-size: 0.8rem;
208      }
209    
210      .description a {
211        padding: 1rem;
212      }
213    
214      .description p,
215      .description div {
216        display: flex;
217        justify-content: center;
218        position: fixed;
219        width: 100%;
220      }
221    
222      .description p {
223        align-items: center;
224        inset: 0 0 auto;
225        padding: 2rem 1rem 1.4rem;
226        border-radius: 0;
227        border: none;
228        border-bottom: 1px solid rgba(var(--callout-border-rgb), 0.25);
229        background: linear-gradient(
230          to bottom,
231          rgba(var(--background-start-rgb), 1),
232          rgba(var(--callout-rgb), 0.5)
233        );
234        background-clip: padding-box;
235        backdrop-filter: blur(24px);
236      }
237    
238      .description div {
239        align-items: flex-end;
240        pointer-events: none;
241        inset: auto 0 0;
242        padding: 2rem;
243        height: 200px;
244        background: linear-gradient(
245          to bottom,
246          transparent 0%,
247          rgb(var(--background-end-rgb)) 40%
248        );
249        z-index: 1;
250      }
251    }
252    
253    @media (prefers-color-scheme: dark) {
254      .vercelLogo {
255        filter: invert(1);
256      }
257    
258      .logo,
259      .thirteen img {
260        filter: invert(1) drop-shadow(0 0 0.3rem #ffffff70);
261      }
262    }
263    
264    @keyframes rotate {
265      from {
266        transform: rotate(360deg);
267      }
268      to {
269        transform: rotate(0deg);
270      }
271    }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/src/app/page.tsx
```tsx
1      import Image from 'next/image'
2      import { Inter } from 'next/font/google'
3      import styles from './page.module.css'
4      
5      const inter = Inter({ subsets: ['latin'] })
6      
7      export default function Home() {
8        return (
9          <main className={styles.main}>
10           <div className={styles.description}>
11             <p>
12               Get started by editing&nbsp;
13               <code className={styles.code}>src/app/page.tsx</code>
14             </p>
15             <div>
16               <a
17                 href="https://vercel.com?utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app"
18                 target="_blank"
19                 rel="noopener noreferrer"
20               >
21                 By{' '}
22                 <Image
23                   src="/vercel.svg"
24                   alt="Vercel Logo"
25                   className={styles.vercelLogo}
26                   width={100}
27                   height={24}
28                   priority
29                 />
30               </a>
31             </div>
32           </div>
33     
34           <div className={styles.center}>
35             <Image
36               className={styles.logo}
37               src="/next.svg"
38               alt="Next.js Logo"
39               width={180}
40               height={37}
41               priority
42             />
43             <div className={styles.thirteen}>
44               <Image src="/thirteen.svg" alt="13" width={40} height={31} priority />
45             </div>
46           </div>
47     
48           <div className={styles.grid}>
49             <a
50               href="https://beta.nextjs.org/docs?utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app"
51               className={styles.card}
52               target="_blank"
53               rel="noopener noreferrer"
54             >
55               <h2 className={inter.className}>
56                 Docs <span>-&gt;</span>
57               </h2>
58               <p className={inter.className}>
59                 Find in-depth information about Next.js features and API.
60               </p>
61             </a>
62     
63             <a
64               href="https://vercel.com/templates?framework=next.js&utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app"
65               className={styles.card}
66               target="_blank"
67               rel="noopener noreferrer"
68             >
69               <h2 className={inter.className}>
70                 Templates <span>-&gt;</span>
71               </h2>
72               <p className={inter.className}>Explore the Next.js 13 playground.</p>
73             </a>
74     
75             <a
76               href="https://vercel.com/new?utm_source=create-next-app&utm_medium=appdir-template&utm_campaign=create-next-app"
77               className={styles.card}
78               target="_blank"
79               rel="noopener noreferrer"
80             >
81               <h2 className={inter.className}>
82                 Deploy <span>-&gt;</span>
83               </h2>
84               <p className={inter.className}>
85                 Instantly deploy your Next.js site to a shareable URL with Vercel.
86               </p>
87             </a>
88           </div>
89         </main>
90       )
91     }
```

<br/>

<!-- NOTE-swimm-snippet: the lines below link your snippet to Swimm -->
### 📄 new-next/tsconfig.json
```json
1      {
2        "compilerOptions": {
3          "target": "es5",
4          "lib": ["dom", "dom.iterable", "esnext"],
5          "allowJs": true,
6          "skipLibCheck": true,
7          "strict": true,
8          "forceConsistentCasingInFileNames": true,
9          "noEmit": true,
10         "esModuleInterop": true,
11         "module": "esnext",
12         "moduleResolution": "node",
13         "resolveJsonModule": true,
14         "isolatedModules": true,
15         "jsx": "preserve",
16         "incremental": true,
17         "plugins": [
18           {
19             "name": "next"
20           }
21         ],
22         "paths": {
23           "@/*": ["./src/*"]
24         }
25       },
26       "include": ["next-env.d.ts", "**/*.ts", "**/*.tsx", ".next/types/**/*.ts"],
27       "exclude": ["node_modules"]
28     }
```

<br/>

This file was generated by Swimm. [Click here to view it in the app](https://app.swimm.io/repos/Z2l0aHViJTNBJTNBdGVzdC1zd2ltbS5pbyUzQSUzQXllbWFybjUxMA==/docs/010sj).
