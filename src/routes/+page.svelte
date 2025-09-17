<script>
    import { GITHUB_USER } from "../lib/constant";

    const works = [
        {
            title: "第34回 高専プロコン 競技部門 優勝",
            desc: "アルゴリズム・UI設計を担当。付随して文部科学大臣賞,情報処理学会若手奨励賞、電子情報通信学会若手奨励賞を受賞。",
            url: `https://github.com/${GITHUB_USER}/procon34_Open`,
            image: null,
        },
        {
            title: "RRT Star Web Simulator",
            desc: "経路計画アルゴリズムのRRT*をWeb上で可視化するシミュレータ。領域分割により高速化。",
            url: `https://${GITHUB_USER}.github.io/RRTStarWebSimulation/`,
            image: null,
        },
        {
            title: "ポートフォリオサイト",
            desc: "SvelteKitで構築しcloudflare pagesでホスティング。",
            url: `https://github.com/${GITHUB_USER}/about-me`,
            image: null,
        },
    ];
</script>

<section class="pt-16">
    <div class="grid items-center gap-10 md:grid-cols-2">
        <div class="row-start-2 md:row-start-auto">
            <h1
                class="text-3xl font-bold tracking-tight text-stone-900 md:text-4xl"
            >
                Tomoya Takahashi
            </h1>
            <p class="mt-4 text-stone-700">
                千葉大学 B3 | <a href="https://akariinc.co.jp/" target="_blank"
                    >燈株式会社</a
                > インターン(2024/9/17〜)
            </p>
        </div>
        <div class="row-start-1 md:row-start-auto flex justify-center">
            <a
                href={`https://github.com/${GITHUB_USER}`}
                target="_blank"
                rel="noopener noreferrer"
                class="group block w-1/2 max-w-[30vh]"
            >
                <img
                    src={`https://github.com/${GITHUB_USER}.png?size=240`}
                    alt={`${GITHUB_USER} のGitHubアバター`}
                    loading="lazy"
                    class="w-full h-auto max-h-[30vh] rounded-2xl object-cover shadow-lg ring-1 ring-yellow-300 transition-transform group-hover:scale-[1.02]"
                />
            </a>
        </div>
    </div>
</section>

<section id="about" class="py-5">
    <p class="leading-7 text-stone-700">
        RustとTypeScriptが好きな大学生です。アルゴリズム高速化や機械学習、ゲームAIに興味があります。
        趣味は漫画と音楽です。
    </p>
</section>

<section id="works" class="pt-8">
    <h2 class="text-2xl font-semibold text-stone-900">制作物等</h2>
    <div class="mt-6 grid gap-6 md:grid-cols-2 px-6">
        {#each works as w}
            {#if w.url}
                <a
                    href={w.url}
                    target="_blank"
                    rel="noopener noreferrer"
                    class="group block rounded-xl border-2 border-yellow-700 bg-white/60 p-5 backdrop-blur hover:bg-white/80 focus:outline-none focus:ring-2 focus:ring-yellow-500 focus:ring-offset-2 focus:ring-offset-yellow-50"
                >
                    {#if w.image}
                        <img
                            src={w.image}
                            alt={w.title}
                            loading="lazy"
                            class="mb-3 aspect-video w-full rounded-lg object-cover ring-1 ring-yellow-200"
                        />
                    {/if}
                    <h3
                        class="font-semibold text-stone-900 group-hover:underline"
                    >
                        {w.title}
                    </h3>
                    <p class="mt-2 text-stone-700">{w.desc}</p>
                </a>
            {:else}
                <article
                    class="rounded-xl border border-yellow-200 bg-white/60 p-5 backdrop-blur"
                >
                    {#if w.image}
                        <img
                            src={w.image}
                            alt={w.title}
                            loading="lazy"
                            class="mb-3 aspect-video w-full rounded-lg object-cover ring-1 ring-yellow-200"
                        />
                    {/if}
                    <h3 class="font-semibold text-stone-900">{w.title}</h3>
                    <p class="mt-2 text-stone-700">{w.desc}</p>
                </article>
            {/if}
        {/each}
    </div>
</section>
