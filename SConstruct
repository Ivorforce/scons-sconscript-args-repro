opts = Variables(None, ARGUMENTS)

opts.Add("my_opt", default="my_opt_default")

framework_env = SConscript("framework/SConstruct")

env = framework_env.Clone()
opts.Update(env)

print(f"My Opt: {env['my_opt']}")
