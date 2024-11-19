opts = Variables(None, ARGUMENTS)

opts.Add("my_opt", default="my_opt_default")

# Remove our custom options to avoid passing to godot-cpp; godot-cpp has its own check for unknown options.
for opt in opts.options:
    ARGUMENTS.pop(opt.key, None)

framework_env = SConscript("framework/SConstruct")

env = framework_env.Clone()
opts.Update(env)

print(f"My Opt: {env['my_opt']}")
