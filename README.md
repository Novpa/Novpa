```typescript
class NovpaGithubProfile {
    private static name = 'Novpa'
    public static role = 'Software Engineer'
    public static motherTongueFE: string[] = ["English"]
    public static motherTongueBE: string[] = ["Logic"]
    public static skills = ["Debugging in Stack Overflow with no AI"]
    public static totalProjects = 5

    constructor() {}

    public static addLanguage(language: string, type: "BE" | "FE"): void {
        if (type === "BE") {
            this.motherTongueBE.push(language)
        } else if (type === "FE") {
            this.motherTongueFE.push(language)
        }
    }
  
    public static printProfile(): void {
        console.log(`I'm ${this.name}, a${this.role}`)
        console.log(`Skills: ${this.skills.join(', ')}`)
        
        console.log(`\nMother Tongue FE:`)
        this.motherTongueFE.forEach(lang => console.log(`> ${lang}`))
    
        console.log(`\nMother Tongue BE:`)
        this.motherTongueBE.forEach(lang => console.log(`> ${lang}`))
    }
}

const feSkills = ["TypeScript", "React.js", "Vue.js", "Next.js", "Tailwind"]
const beSkills = ["Node.js", "Express.js", "SQL", "NoSQL", "Git", "Docker", "Redis"]

feSkills.forEach(skill => NovpaGithubProfile.addLanguage(skill, "FE"))
beSkills.forEach(skill => NovpaGithubProfile.addLanguage(skill, "BE"))

NovpaGithubProfile.printProfile()
```


![Snake Game](https://github.com/Novpa/Novpa/blob/main/github-snake.svg)

