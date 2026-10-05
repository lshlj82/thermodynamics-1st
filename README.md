# Temperature, Heat, and the First Law of Thermodynamics

This is an interactive, browser-based demo of the first part of thermodynamics. It covers temperature and the zeroth law, thermal expansion, heat and specific heat, phase changes, work done by a gas, the first law, heat transfer, the ideal gas, and the kinetic theory of gases. It comes as two separate pages, one in English and one in Korean.

Created by **Claude Opus 5.5**, based on the lecture notes by **Sang Hoon Lee (이상훈)**.

> **한국어 요약:** 온도와 열역학 제0법칙, 열팽창, 열과 비열, 변환열, 기체가 한 일, 열역학 제1법칙과 그 특수한 경우, 열전달(전도·대류·복사), 이상기체, 이상기체가 한 일, 압력과 제곱평균제곱근 속력, Maxwell 속력분포, 몰비열, 자유도, 단열팽창을 직접 조작해 볼 수 있는 인터랙티브 웹 데모입니다. 이상훈(Sang Hoon Lee)의 강의 노트를 바탕으로 Claude Opus 5.5가 만들었습니다. 한국어 페이지는 `thermo1-ko.html`입니다.

## Files

| File | Description |
| --- | --- |
| `thermo1-en.html` | American English version |
| `thermo1-ko.html` | Korean version (한국어) |
| `README.md` | This file |

Each page is a single self-contained HTML file with inline CSS and JavaScript. There is no build step and there are no dependencies. The only external request is to Google Fonts for IBM Plex Sans KR. If that request fails, the page falls back to system fonts. Each page links to the other language from its top bar. Equations use real fraction bars, radical signs, and stacked sub- and superscripts, and halves are written as (1/2).

## Running it

Open either file directly in a modern browser, or serve the folder locally:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/thermo1-en.html
```

### Publishing on GitHub Pages

1. Push these files to a repository.
2. In **Settings → Pages**, choose **Deploy from a branch**, then select your branch and the root folder.
3. Visit `https://<user>.github.io/<repo>/thermo1-en.html` or `.../thermo1-ko.html`.

These pages can share a repository with the other demos in the series (`motion-*`, `newton-*`, `energy-*`, `momentum-*`, `rotation-*`, `oscillation-wave-*`, `thermo2-*`, `gauss-*`, `circuits-*`, `rc-*`, `magnetism-*`, `induction-*`, `maxwell-*`). The file names don't collide. The second part of thermodynamics, on entropy and the second law, is `thermo2-*`.

## What's inside

The fifteen sections follow the order of the lecture notes. Every value is recomputed live as you move the controls.

1. **Temperature and the zeroth law:** Bodies A and B and a small thermometer T can be put in contact in pairs. Heat flows from the hotter to the colder body until they reach thermal equilibrium. The thermometer reads in K, °C and °F, and the page reports whether A and B are in thermal equilibrium.
2. **Thermal expansion:** A brass–steel strip ($\alpha = 19\times10^{-6}$ and $11\times10^{-6}$ /°C) bends as its temperature changes. The page gives $\Delta L=\alpha L\Delta T$ for each metal, the tip deflection, and compares $\Delta V/V \approx 3\alpha\Delta T$ with the exact value.
3. **Heat and specific heat:** The same heater power warms a chosen material and the same mass of water side by side. The page gives $c$, $C=cm$, $Q=Pt$, and both temperatures, using the table of specific heats from the notes. Negative power cools both.
4. **Heats of transformation:** Ice at −20 °C is heated at constant power until it is steam at 120 °C. The $T$–$Q$ graph shows flat stretches where $Q=L_Fm$ and $Q=L_Vm$ are absorbed, and a beaker shows ice, water and steam.
5. **Work done by a gas:** A gas in a cylinder moves along the six paths (a)–(f) from the notes: a curve, expanding first, dropping the pressure first, an adjustable intermediate pressure, the reverse path, and a clockwise cycle. $W=\int p\,dV$ is shaded as the area under the path, or inside the cycle.
6. **The first law:** One mole of a monatomic ideal gas goes between the same two states along three paths. A table shows that $Q$ and $W$ depend on the path while $Q-W=\Delta E_\text{int}$ does not.
7. **Special cases:** Adiabatic ($Q=0$), constant-volume ($W=0$), cyclic ($\Delta E_\text{int}=0$), and free expansion ($Q=W=\Delta E_\text{int}=0$). Free expansion shows the gas spreading through an opened stopcock, with only the endpoints drawn on the $p$–$V$ diagram.
8. **Heat transfer:** Conduction through a slab of a chosen material gives $P_\text{cond}=kA(T_H-T_C)/L$ and $R=L/k$, with heat packets crossing the slab. Radiation from a body gives $P_\text{rad}=\sigma\varepsilon AT^4$, and the body glows once it is hot enough.
9. **The ideal gas:** A gas in a cylinder with particles whose speed follows $\sqrt T$. You hold $T$, $p$ or $V$ constant (Boyle, Charles, Gay-Lussac), and the state leaves a trail on the $p$–$V$ diagram. The page checks that $pV=nRT=NkT$.
10. **Work done by an ideal gas:** Isothermal ($W=nRT\ln(V_f/V_i)$), isobaric ($W=p\Delta V$) and isochoric ($W=0$) processes. The page compares the formula with the area added up numerically.
11. **Pressure and RMS speed:** Molecules bounce in a box and the simulation counts the momentum they deliver to the right wall. The measured pressure settles to within about 1% of $Nm(v_x^2)_\text{avg}/V$. The page gives $v_\text{rms}=\sqrt{3RT/M}$ for hydrogen, helium, nitrogen, oxygen and carbon dioxide.
12. **Speed distribution:** The Maxwell distribution at two temperatures (300 K and 80 K by default, as in the notes' figure). The page marks $v_p$, $v_\text{avg}$ and $v_\text{rms}$, shades the fraction of molecules between two speeds, and gives $K_\text{avg}=\tfrac32 kT$.
13. **Molar specific heats:** The same heat goes into two cylinders, one with its piston pinned (constant volume) and one with a free piston (constant pressure). Bars show $\Delta E_\text{int}$ and $W$. The page gives $C_V$, $C_p=C_V+R$, both temperature rises, and $\gamma$.
14. **Degrees of freedom:** $C_V/R$ against temperature for a monatomic or diatomic gas, with an animated molecule whose rotation and vibration switch on as the temperature rises.
15. **Adiabatic expansion:** An adiabat $pV^\gamma=\text{const}$ for $\gamma = 5/3$ or $7/5$, compared with the 300, 500 and 700 K isotherms and with the isotherm through the starting point. The page gives $p_f$, $T_f$ (from $TV^{\gamma-1}=\text{const}$) and $W$. A free-expansion option keeps $T_f=T_i$ and draws only the endpoints.

The header animation shows a gas in a cylinder running a cycle. Heat flows in or out at the bottom, the piston does work, and a dot traces the same cycle on a $p$–$V$ diagram, next to $\Delta E_\text{int}=Q-W$.

## Notes on the model

- **Sign convention:** $W$ is the work done **by** the gas, as in the notes, so the first law reads $\Delta E_\text{int}=Q-W$.
- **Corrections to the notes:** Two formulas in the notes have small typos. The pages use the per-mole forms $C_p=\tfrac52 R$ and $\Delta E_\text{int}=nC_V\Delta T$.
- **Added values:** A few values are not in the notes. The specific heat of steam (about 2010 J/(kg·K)) is used in the heating curve, and section 8 uses standard thermal conductivities for its slab materials.
- **Schematic curve:** The steps in the degrees-of-freedom curve show the shape of the behavior; their exact temperatures are illustrative.
- **Simplified pressure model:** In section 11 the molecules move in a flat, two-dimensional box and don't collide with each other, as the notes assume for an ideal gas.
- **Animation speed:** The heating curve runs 200 times faster than real time, and the page says so on screen. The readouts always show the real values.
- **Units:** In the $p$–$V$ sections, volumes are in liters and pressures in kilopascals, so 1 kPa·L = 1 J.
- **Display:** The pages follow the system's light or dark setting. Under `prefers-reduced-motion`, the animations start paused and can be played by hand. Only simulations that are currently on screen are animated.

## Credits

- Lecture notes: Sang Hoon Lee (이상훈)
- Demo design and code: Claude Opus 5.5

## License

No license has been chosen yet. Before publishing, add a `LICENSE` file if you want others to be able to reuse the code. Also confirm with the author of the lecture notes how their material may be shared.
